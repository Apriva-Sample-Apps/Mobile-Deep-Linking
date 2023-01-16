# Mobile-Deep-Linking
AprivaPay Mobile - Deep Linking Sample
Android and iOS sample code and documentation contained within download files. 

Deep Linking: Mobile Pay by HGPay - Android
URL Format
Below are the URLs used for deep linking in Mobile Pay by HGPay. In the URL, the ###
should be replaced with the minor units representing the transaction amount. For
example, $1.23 would be represented as 123 in minor units.
https://pagomovil.hgpay.com.mx/dl/sale?amount=###
Sample Code
Kotlin
fun launchDeepLink(amount: Int){
val uri = Uri.parse("https://pagomovil.hgpay.com.mx/dl/sale?amount=$amount")
val intent = Intent(Intent.ACTION_VIEW, uri)
intent.addCategory(Intent.CATEGORY_DEFAULT) // optional
intent.addCategory(Intent.CATEGORY_BROWSABLE) // optional
/*
* Note that if the context is not android.app.Activity Context,
* then the Intent must include the Intent.FLAG_ACTIVITY_NEW_TASK launch flag
*/
intent.flags = Intent.FLAG_ACTIVITY_NEW_TASK
context.startActivity(intent)
}
Java
public void launchDeepLink(int amount) {
Uri uri = Uri.parse("https://pagomovil.hgpay.com.mx/dl/sale?amount="+ amount);
Intent intent = new Intent(Intent.ACTION_VIEW, uri);
intent.addCategory(Intent.CATEGORY_DEFAULT); // optional
intent.addCategory(Intent.CATEGORY_BROWSABLE); // optional
/*
* Note that if the context is not android.app.Activity Context,
* then the Intent must include the Intent.FLAG_ACTIVITY_NEW_TASK launch flag
*/
intent.setFlags(Intent.FLAG_ACTIVITY_NEW_TASK);
context.startActivity(intent);
}
