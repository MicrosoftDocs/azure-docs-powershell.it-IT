---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 33efe02dd463334745e39d846d0b43c2ccd9dd6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687552"
---
# <span data-ttu-id="b8e77-101">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="b8e77-101">New-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="b8e77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8e77-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e77-103">Crea un binding a un certificato SSL per una Web App Azure.</span><span class="sxs-lookup"><span data-stu-id="b8e77-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8e77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8e77-104">SYNTAX</span></span>

### <span data-ttu-id="b8e77-105">S1</span><span class="sxs-lookup"><span data-stu-id="b8e77-105">S1</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8e77-106">S2</span><span class="sxs-lookup"><span data-stu-id="b8e77-106">S2</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8e77-107">S3</span><span class="sxs-lookup"><span data-stu-id="b8e77-107">S3</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8e77-108">S4</span><span class="sxs-lookup"><span data-stu-id="b8e77-108">S4</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8e77-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8e77-109">DESCRIPTION</span></span>
<span data-ttu-id="b8e77-110">Il cmdlet **New-AzureRmWebAppSSLBinding** crea un binding di certificato SSL (Secure Socket Layer) per un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="b8e77-110">The **New-AzureRmWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="b8e77-111">Il cmdlet crea un binding SSL in due modi:</span><span class="sxs-lookup"><span data-stu-id="b8e77-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="b8e77-112">Puoi associare un'app Web a un certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="b8e77-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="b8e77-113">Puoi caricare un nuovo certificato e quindi associare l'app Web a questo nuovo certificato.</span><span class="sxs-lookup"><span data-stu-id="b8e77-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="b8e77-114">Indipendentemente dall'approccio usato, il certificato e l'app Web devono essere associati allo stesso gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="b8e77-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="b8e77-115">Se si ha un'app Web nel gruppo di risorse a e si vuole associare l'app Web a un certificato nel gruppo di risorse B, l'unico modo per eseguire questa operazione consiste nel caricare una copia del certificato nel gruppo di risorse A. Se si carica un nuovo certificato, ricordare i requisiti seguenti per un certificato SSL di Azure:</span><span class="sxs-lookup"><span data-stu-id="b8e77-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="b8e77-116">Il certificato deve contenere una chiave privata.</span><span class="sxs-lookup"><span data-stu-id="b8e77-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="b8e77-117">Il certificato deve usare il formato PFX (Personal Information Exchange).</span><span class="sxs-lookup"><span data-stu-id="b8e77-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="b8e77-118">Il nome dell'oggetto del certificato deve corrispondere al dominio usato per accedere all'app Web.</span><span class="sxs-lookup"><span data-stu-id="b8e77-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="b8e77-119">Il certificato deve usare un minimo di crittografia a 2048 bit.</span><span class="sxs-lookup"><span data-stu-id="b8e77-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="b8e77-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8e77-120">EXAMPLES</span></span>

### <span data-ttu-id="b8e77-121">Esempio 1: associare un certificato a un'app Web</span><span class="sxs-lookup"><span data-stu-id="b8e77-121">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="b8e77-122">Questo comando associa un certificato Azure esistente (un certificato con l'identificazione personale E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) all'app Web denominata ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="b8e77-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

## <span data-ttu-id="b8e77-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8e77-123">PARAMETERS</span></span>

### <span data-ttu-id="b8e77-124">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="b8e77-124">-CertificateFilePath</span></span>
<span data-ttu-id="b8e77-125">Specifica il percorso del file per il certificato da caricare.</span><span class="sxs-lookup"><span data-stu-id="b8e77-125">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="b8e77-126">Il parametro *CertificateFilePath* è obbligatorio solo se il certificato non è stato ancora caricato in Azure.</span><span class="sxs-lookup"><span data-stu-id="b8e77-126">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

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

### <span data-ttu-id="b8e77-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b8e77-127">-CertificatePassword</span></span>
<span data-ttu-id="b8e77-128">Specifica la password di decrittografia per il certificato.</span><span class="sxs-lookup"><span data-stu-id="b8e77-128">Specifies the decryption password for the certificate.</span></span>

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

### <span data-ttu-id="b8e77-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8e77-129">-DefaultProfile</span></span>
<span data-ttu-id="b8e77-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b8e77-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e77-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8e77-131">-Name</span></span>
<span data-ttu-id="b8e77-132">Specifica il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="b8e77-132">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="b8e77-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8e77-133">-ResourceGroupName</span></span>
<span data-ttu-id="b8e77-134">Specifica il nome del gruppo di risorse a cui è assegnato il certificato.</span><span class="sxs-lookup"><span data-stu-id="b8e77-134">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="b8e77-135">Non è possibile usare il parametro *ResourceGroupName* e il parametro *Web App* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="b8e77-135">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="b8e77-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="b8e77-136">-Slot</span></span>
<span data-ttu-id="b8e77-137">Specifica il nome dello slot di distribuzione dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="b8e77-137">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="b8e77-138">Puoi usare il cmdlet Get-AzureRMWebAppSlot per ottenere uno slot.</span><span class="sxs-lookup"><span data-stu-id="b8e77-138">You can use the Get-AzureRMWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="b8e77-139">Gli slot di distribuzione consentono di organizzare e convalidare le app Web senza che le app siano accessibili tramite Internet.</span><span class="sxs-lookup"><span data-stu-id="b8e77-139">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="b8e77-140">In genere, le modifiche verranno distribuite in un sito di staging, convalidarle e quindi distribuirle nel sito di produzione (accessibile tramite Internet).</span><span class="sxs-lookup"><span data-stu-id="b8e77-140">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

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

### <span data-ttu-id="b8e77-141">-SslState</span><span class="sxs-lookup"><span data-stu-id="b8e77-141">-SslState</span></span>
<span data-ttu-id="b8e77-142">Specifica se il certificato è abilitato.</span><span class="sxs-lookup"><span data-stu-id="b8e77-142">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="b8e77-143">Imposta il parametro *SSLState* su 1 per abilitare il certificato oppure imposta *SSLState* su 0 per disabilitare il certificato.</span><span class="sxs-lookup"><span data-stu-id="b8e77-143">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

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

### <span data-ttu-id="b8e77-144">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="b8e77-144">-Thumbprint</span></span>
<span data-ttu-id="b8e77-145">Specifica l'identificatore univoco per il certificato.</span><span class="sxs-lookup"><span data-stu-id="b8e77-145">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="b8e77-146">-Web App</span><span class="sxs-lookup"><span data-stu-id="b8e77-146">-WebApp</span></span>
<span data-ttu-id="b8e77-147">Specifica un'app Web.</span><span class="sxs-lookup"><span data-stu-id="b8e77-147">Specifies a Web App.</span></span>
<span data-ttu-id="b8e77-148">Per ottenere un'app Web, usa il cmdlet Get-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="b8e77-148">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>
<span data-ttu-id="b8e77-149">Non è possibile usare il parametro *Web App* nello stesso comando del parametro *ResourceGroupName* e/o *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="b8e77-149">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="b8e77-150">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="b8e77-150">-WebAppName</span></span>
<span data-ttu-id="b8e77-151">Specifica il nome dell'app Web per cui è in corso la creazione del nuovo binding SSL.</span><span class="sxs-lookup"><span data-stu-id="b8e77-151">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="b8e77-152">Non è possibile usare il parametro *WebAppName* e il parametro *Web App* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="b8e77-152">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="b8e77-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8e77-153">CommonParameters</span></span>
<span data-ttu-id="b8e77-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8e77-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8e77-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8e77-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8e77-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8e77-156">INPUTS</span></span>

### <span data-ttu-id="b8e77-157">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="b8e77-157">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="b8e77-158">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b8e77-158">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="b8e77-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8e77-159">OUTPUTS</span></span>

### <span data-ttu-id="b8e77-160">Microsoft. Azure. Management. website. Models. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="b8e77-160">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="b8e77-161">Note</span><span class="sxs-lookup"><span data-stu-id="b8e77-161">NOTES</span></span>

## <span data-ttu-id="b8e77-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8e77-162">RELATED LINKS</span></span>

[<span data-ttu-id="b8e77-163">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="b8e77-163">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="b8e77-164">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="b8e77-164">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="b8e77-165">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b8e77-165">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="b8e77-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b8e77-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


