---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: ed0e0f0ddf42266921113b219d81cfd5b6b6417c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676284"
---
# <span data-ttu-id="f8a24-101">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f8a24-101">New-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="f8a24-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8a24-102">SYNOPSIS</span></span>
<span data-ttu-id="f8a24-103">Crea un binding a un certificato SSL per una Web App Azure.</span><span class="sxs-lookup"><span data-stu-id="f8a24-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

## <span data-ttu-id="f8a24-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8a24-104">SYNTAX</span></span>

### <span data-ttu-id="f8a24-105">S1</span><span class="sxs-lookup"><span data-stu-id="f8a24-105">S1</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8a24-106">S2</span><span class="sxs-lookup"><span data-stu-id="f8a24-106">S2</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8a24-107">S3</span><span class="sxs-lookup"><span data-stu-id="f8a24-107">S3</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8a24-108">S4</span><span class="sxs-lookup"><span data-stu-id="f8a24-108">S4</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8a24-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8a24-109">DESCRIPTION</span></span>
<span data-ttu-id="f8a24-110">Il cmdlet **New-AzWebAppSSLBinding** crea un binding di certificato SSL (Secure Socket Layer) per un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="f8a24-110">The **New-AzWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="f8a24-111">Il cmdlet crea un binding SSL in due modi:</span><span class="sxs-lookup"><span data-stu-id="f8a24-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="f8a24-112">Puoi associare un'app Web a un certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="f8a24-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="f8a24-113">Puoi caricare un nuovo certificato e quindi associare l'app Web a questo nuovo certificato.</span><span class="sxs-lookup"><span data-stu-id="f8a24-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="f8a24-114">Indipendentemente dall'approccio usato, il certificato e l'app Web devono essere associati allo stesso gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="f8a24-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="f8a24-115">Se si ha un'app Web nel gruppo di risorse a e si vuole associare l'app Web a un certificato nel gruppo di risorse B, l'unico modo per eseguire questa operazione consiste nel caricare una copia del certificato nel gruppo di risorse A. Se si carica un nuovo certificato, ricordare i requisiti seguenti per un certificato SSL di Azure:</span><span class="sxs-lookup"><span data-stu-id="f8a24-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="f8a24-116">Il certificato deve contenere una chiave privata.</span><span class="sxs-lookup"><span data-stu-id="f8a24-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="f8a24-117">Il certificato deve usare il formato PFX (Personal Information Exchange).</span><span class="sxs-lookup"><span data-stu-id="f8a24-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="f8a24-118">Il nome dell'oggetto del certificato deve corrispondere al dominio usato per accedere all'app Web.</span><span class="sxs-lookup"><span data-stu-id="f8a24-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="f8a24-119">Il certificato deve usare un minimo di crittografia a 2048 bit.</span><span class="sxs-lookup"><span data-stu-id="f8a24-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="f8a24-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8a24-120">EXAMPLES</span></span>

### <span data-ttu-id="f8a24-121">Esempio 1: associare un certificato a un'app Web</span><span class="sxs-lookup"><span data-stu-id="f8a24-121">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="f8a24-122">Questo comando associa un certificato Azure esistente (un certificato con l'identificazione personale E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) all'app Web denominata ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="f8a24-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

## <span data-ttu-id="f8a24-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8a24-123">PARAMETERS</span></span>

### <span data-ttu-id="f8a24-124">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="f8a24-124">-CertificateFilePath</span></span>
<span data-ttu-id="f8a24-125">Specifica il percorso del file per il certificato da caricare.</span><span class="sxs-lookup"><span data-stu-id="f8a24-125">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="f8a24-126">Il parametro *CertificateFilePath* è obbligatorio solo se il certificato non è stato ancora caricato in Azure.</span><span class="sxs-lookup"><span data-stu-id="f8a24-126">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

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

### <span data-ttu-id="f8a24-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f8a24-127">-CertificatePassword</span></span>
<span data-ttu-id="f8a24-128">Specifica la password di decrittografia per il certificato.</span><span class="sxs-lookup"><span data-stu-id="f8a24-128">Specifies the decryption password for the certificate.</span></span>

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

### <span data-ttu-id="f8a24-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8a24-129">-DefaultProfile</span></span>
<span data-ttu-id="f8a24-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8a24-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8a24-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8a24-131">-Name</span></span>
<span data-ttu-id="f8a24-132">Specifica il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="f8a24-132">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="f8a24-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8a24-133">-ResourceGroupName</span></span>
<span data-ttu-id="f8a24-134">Specifica il nome del gruppo di risorse a cui è assegnato il certificato.</span><span class="sxs-lookup"><span data-stu-id="f8a24-134">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="f8a24-135">Non è possibile usare il parametro *ResourceGroupName* e il parametro *Web App* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="f8a24-135">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="f8a24-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="f8a24-136">-Slot</span></span>
<span data-ttu-id="f8a24-137">Specifica il nome dello slot di distribuzione dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="f8a24-137">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="f8a24-138">Puoi usare il cmdlet Get-AzWebAppSlot per ottenere uno slot.</span><span class="sxs-lookup"><span data-stu-id="f8a24-138">You can use the Get-AzWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="f8a24-139">Gli slot di distribuzione consentono di organizzare e convalidare le app Web senza che le app siano accessibili tramite Internet.</span><span class="sxs-lookup"><span data-stu-id="f8a24-139">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="f8a24-140">In genere, le modifiche verranno distribuite in un sito di staging, convalidarle e quindi distribuirle nel sito di produzione (accessibile tramite Internet).</span><span class="sxs-lookup"><span data-stu-id="f8a24-140">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

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

### <span data-ttu-id="f8a24-141">-SslState</span><span class="sxs-lookup"><span data-stu-id="f8a24-141">-SslState</span></span>
<span data-ttu-id="f8a24-142">Specifica se il certificato è abilitato.</span><span class="sxs-lookup"><span data-stu-id="f8a24-142">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="f8a24-143">Imposta il parametro *SSLState* su 1 per abilitare il certificato oppure imposta *SSLState* su 0 per disabilitare il certificato.</span><span class="sxs-lookup"><span data-stu-id="f8a24-143">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

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

### <span data-ttu-id="f8a24-144">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="f8a24-144">-Thumbprint</span></span>
<span data-ttu-id="f8a24-145">Specifica l'identificatore univoco per il certificato.</span><span class="sxs-lookup"><span data-stu-id="f8a24-145">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="f8a24-146">-Web App</span><span class="sxs-lookup"><span data-stu-id="f8a24-146">-WebApp</span></span>
<span data-ttu-id="f8a24-147">Specifica un'app Web.</span><span class="sxs-lookup"><span data-stu-id="f8a24-147">Specifies a Web App.</span></span>
<span data-ttu-id="f8a24-148">Per ottenere un'app Web, usa il cmdlet Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="f8a24-148">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="f8a24-149">Non è possibile usare il parametro *Web App* nello stesso comando del parametro *ResourceGroupName* e/o *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="f8a24-149">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="f8a24-150">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="f8a24-150">-WebAppName</span></span>
<span data-ttu-id="f8a24-151">Specifica il nome dell'app Web per cui è in corso la creazione del nuovo binding SSL.</span><span class="sxs-lookup"><span data-stu-id="f8a24-151">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="f8a24-152">Non è possibile usare il parametro *WebAppName* e il parametro *Web App* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="f8a24-152">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="f8a24-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8a24-153">CommonParameters</span></span>
<span data-ttu-id="f8a24-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8a24-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8a24-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8a24-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8a24-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8a24-156">INPUTS</span></span>

### <span data-ttu-id="f8a24-157">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="f8a24-157">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f8a24-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8a24-158">OUTPUTS</span></span>

### <span data-ttu-id="f8a24-159">Microsoft. Azure. Management. website. Models. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="f8a24-159">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="f8a24-160">Note</span><span class="sxs-lookup"><span data-stu-id="f8a24-160">NOTES</span></span>

## <span data-ttu-id="f8a24-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8a24-161">RELATED LINKS</span></span>

[<span data-ttu-id="f8a24-162">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f8a24-162">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="f8a24-163">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f8a24-163">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="f8a24-164">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f8a24-164">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="f8a24-165">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f8a24-165">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

