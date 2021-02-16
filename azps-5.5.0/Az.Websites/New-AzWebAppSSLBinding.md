---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 2fff18033febbab23083127628959d2fca9305a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208866"
---
# <span data-ttu-id="a9da0-101">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a9da0-101">New-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="a9da0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9da0-102">SYNOPSIS</span></span>
<span data-ttu-id="a9da0-103">Crea un binding di certificato SSL per un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="a9da0-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

## <span data-ttu-id="a9da0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9da0-104">SYNTAX</span></span>

### <span data-ttu-id="a9da0-105">S1</span><span class="sxs-lookup"><span data-stu-id="a9da0-105">S1</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9da0-106">S2</span><span class="sxs-lookup"><span data-stu-id="a9da0-106">S2</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9da0-107">S3</span><span class="sxs-lookup"><span data-stu-id="a9da0-107">S3</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9da0-108">S4</span><span class="sxs-lookup"><span data-stu-id="a9da0-108">S4</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9da0-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a9da0-109">DESCRIPTION</span></span>
<span data-ttu-id="a9da0-110">Il cmdlet **New-AzWebAppSSLBinding** crea un binding di certificato SSL (Secure Socket Layer) per un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="a9da0-110">The **New-AzWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="a9da0-111">Il cmdlet crea un binding SSL in due modi:</span><span class="sxs-lookup"><span data-stu-id="a9da0-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="a9da0-112">È possibile associare un'app Web a un certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="a9da0-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="a9da0-113">È possibile caricare un nuovo certificato e quindi associare l'app Web al nuovo certificato.</span><span class="sxs-lookup"><span data-stu-id="a9da0-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="a9da0-114">Indipendentemente dall'approccio in uso, il certificato e l'app Web devono essere associati allo stesso gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="a9da0-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="a9da0-115">Se si ha un'app Web nel gruppo di risorse A e si vuole associarla a un certificato nel gruppo di risorse B, l'unico modo per farlo è caricare una copia del certificato nel gruppo di risorse A. Se si carica un nuovo certificato, tenere presente i requisiti seguenti per un certificato SSL di Azure:</span><span class="sxs-lookup"><span data-stu-id="a9da0-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="a9da0-116">Il certificato deve contenere una chiave privata.</span><span class="sxs-lookup"><span data-stu-id="a9da0-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="a9da0-117">Il certificato deve usare il formato PFX (Personal Information Exchange).</span><span class="sxs-lookup"><span data-stu-id="a9da0-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="a9da0-118">Il nome dell'oggetto del certificato deve corrispondere al dominio usato per accedere all'app Web.</span><span class="sxs-lookup"><span data-stu-id="a9da0-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="a9da0-119">Il certificato deve usare una crittografia minima a 2048 bit.</span><span class="sxs-lookup"><span data-stu-id="a9da0-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="a9da0-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9da0-120">EXAMPLES</span></span>

### <span data-ttu-id="a9da0-121">Esempio 1: Associare un certificato a un'app Web</span><span class="sxs-lookup"><span data-stu-id="a9da0-121">Example 1: Bind a certificate to a Web App</span></span>
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="a9da0-122">Questo comando associa un certificato di Azure esistente (un certificato con Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) all'app Web denominata ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="a9da0-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

### <span data-ttu-id="a9da0-123">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a9da0-123">Example 2</span></span>

<span data-ttu-id="a9da0-124">Crea un binding di certificato SSL per un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="a9da0-124">Creates an SSL certificate binding for an Azure Web App.</span></span> <span data-ttu-id="a9da0-125">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="a9da0-125">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## <span data-ttu-id="a9da0-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9da0-126">PARAMETERS</span></span>

### <span data-ttu-id="a9da0-127">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="a9da0-127">-CertificateFilePath</span></span>
<span data-ttu-id="a9da0-128">Specifica il percorso del file per il certificato da caricare.</span><span class="sxs-lookup"><span data-stu-id="a9da0-128">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="a9da0-129">Il *parametro CertificateFilePath* è necessario solo se il certificato non è ancora stato caricato in Azure.</span><span class="sxs-lookup"><span data-stu-id="a9da0-129">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9da0-130">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a9da0-130">-CertificatePassword</span></span>
<span data-ttu-id="a9da0-131">Specifica la password di decrittografia per il certificato.</span><span class="sxs-lookup"><span data-stu-id="a9da0-131">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9da0-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9da0-132">-DefaultProfile</span></span>
<span data-ttu-id="a9da0-133">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9da0-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9da0-134">-Name</span><span class="sxs-lookup"><span data-stu-id="a9da0-134">-Name</span></span>
<span data-ttu-id="a9da0-135">Specifica il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="a9da0-135">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9da0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9da0-136">-ResourceGroupName</span></span>
<span data-ttu-id="a9da0-137">Specifica il nome del gruppo di risorse a cui è assegnato il certificato.</span><span class="sxs-lookup"><span data-stu-id="a9da0-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="a9da0-138">Non è possibile usare *il parametro ResourceGroupName* e il *parametro WebApp* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="a9da0-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9da0-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="a9da0-139">-Slot</span></span>
<span data-ttu-id="a9da0-140">Specifica il nome dello slot di distribuzione dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="a9da0-140">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="a9da0-141">È possibile usare il cmdlet Get-AzWebAppSlot per ottenere uno slot.</span><span class="sxs-lookup"><span data-stu-id="a9da0-141">You can use the Get-AzWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="a9da0-142">Gli slot di distribuzione consentono di eseguire stage e convalidare app Web senza che siano accessibili tramite Internet.</span><span class="sxs-lookup"><span data-stu-id="a9da0-142">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="a9da0-143">In genere le modifiche vengono distribuite in un sito di gestione temporanea, vengono convalidate e quindi distribuite nel sito di produzione (accessibile tramite Internet).</span><span class="sxs-lookup"><span data-stu-id="a9da0-143">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9da0-144">-SslState</span><span class="sxs-lookup"><span data-stu-id="a9da0-144">-SslState</span></span>
<span data-ttu-id="a9da0-145">Specifica se il certificato è abilitato.</span><span class="sxs-lookup"><span data-stu-id="a9da0-145">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="a9da0-146">Impostare il *parametro SSLState* su 1 per abilitare il certificato oppure su *SSLState* su 0 per disabilitare il certificato.</span><span class="sxs-lookup"><span data-stu-id="a9da0-146">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9da0-147">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="a9da0-147">-Thumbprint</span></span>
<span data-ttu-id="a9da0-148">Specifica l'identificatore univoco per il certificato.</span><span class="sxs-lookup"><span data-stu-id="a9da0-148">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9da0-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a9da0-149">-WebApp</span></span>
<span data-ttu-id="a9da0-150">Specifica un'app Web.</span><span class="sxs-lookup"><span data-stu-id="a9da0-150">Specifies a Web App.</span></span>
<span data-ttu-id="a9da0-151">Per ottenere un'app Web, usare il cmdlet Get-AzWebApp web app.</span><span class="sxs-lookup"><span data-stu-id="a9da0-151">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="a9da0-152">Non è possibile usare *il parametro WebApp* nello stesso comando del parametro *ResourceGroupName* e/o *WebAppName.*</span><span class="sxs-lookup"><span data-stu-id="a9da0-152">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S3, S4
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9da0-153">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="a9da0-153">-WebAppName</span></span>
<span data-ttu-id="a9da0-154">Specifica il nome dell'app Web per cui viene creata la nuova associazione SSL.</span><span class="sxs-lookup"><span data-stu-id="a9da0-154">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="a9da0-155">Non è possibile usare *il parametro WebAppName* e il *parametro WebApp* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="a9da0-155">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9da0-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9da0-156">CommonParameters</span></span>
<span data-ttu-id="a9da0-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9da0-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9da0-158">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9da0-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9da0-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="a9da0-159">INPUTS</span></span>

### <span data-ttu-id="a9da0-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="a9da0-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a9da0-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9da0-161">OUTPUTS</span></span>

### <span data-ttu-id="a9da0-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="a9da0-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="a9da0-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="a9da0-163">NOTES</span></span>

## <span data-ttu-id="a9da0-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9da0-164">RELATED LINKS</span></span>

[<span data-ttu-id="a9da0-165">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a9da0-165">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="a9da0-166">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a9da0-166">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="a9da0-167">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a9da0-167">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="a9da0-168">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a9da0-168">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


