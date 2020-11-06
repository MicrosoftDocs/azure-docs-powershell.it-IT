---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 99d7d4a0feeb0f548ef65d06234eecb1ad2baf6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521497"
---
# <span data-ttu-id="e6e53-101">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="e6e53-101">New-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="e6e53-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6e53-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e53-103">Crea un binding a un certificato SSL per una Web App Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e53-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6e53-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6e53-104">SYNTAX</span></span>

### <span data-ttu-id="e6e53-105">S1</span><span class="sxs-lookup"><span data-stu-id="e6e53-105">S1</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6e53-106">S2</span><span class="sxs-lookup"><span data-stu-id="e6e53-106">S2</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6e53-107">S3</span><span class="sxs-lookup"><span data-stu-id="e6e53-107">S3</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6e53-108">S4</span><span class="sxs-lookup"><span data-stu-id="e6e53-108">S4</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6e53-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6e53-109">DESCRIPTION</span></span>
<span data-ttu-id="e6e53-110">Il cmdlet **New-AzureRmWebAppSSLBinding** crea un binding di certificato SSL (Secure Socket Layer) per un'app Azure Web.</span><span class="sxs-lookup"><span data-stu-id="e6e53-110">The **New-AzureRmWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="e6e53-111">Il cmdlet crea un binding SSL in due modi:</span><span class="sxs-lookup"><span data-stu-id="e6e53-111">The cmdlet creates an SSL binding in two ways:</span></span> 

- <span data-ttu-id="e6e53-112">Puoi associare un'app Web a un certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="e6e53-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="e6e53-113">Puoi caricare un nuovo certificato e quindi associare l'app Web a questo nuovo certificato.</span><span class="sxs-lookup"><span data-stu-id="e6e53-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>

<span data-ttu-id="e6e53-114">Indipendentemente dall'approccio usato, il certificato e l'app Web devono essere associati allo stesso gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e53-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="e6e53-115">Se si ha un'app Web nel gruppo di risorse a e si vuole associare l'app Web a un certificato nel gruppo di risorse B, l'unico modo per eseguire questa operazione consiste nel caricare una copia del certificato nel gruppo di risorse A.</span><span class="sxs-lookup"><span data-stu-id="e6e53-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A.</span></span>

<span data-ttu-id="e6e53-116">Se si carica un nuovo certificato, ricordare i requisiti seguenti per un certificato SSL di Azure:</span><span class="sxs-lookup"><span data-stu-id="e6e53-116">If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 

- <span data-ttu-id="e6e53-117">Il certificato deve contenere una chiave privata.</span><span class="sxs-lookup"><span data-stu-id="e6e53-117">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="e6e53-118">Il certificato deve usare il formato PFX (Personal Information Exchange).</span><span class="sxs-lookup"><span data-stu-id="e6e53-118">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="e6e53-119">Il nome dell'oggetto del certificato deve corrispondere al dominio usato per accedere all'app Web.</span><span class="sxs-lookup"><span data-stu-id="e6e53-119">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="e6e53-120">Il certificato deve usare un minimo di crittografia a 2048 bit.</span><span class="sxs-lookup"><span data-stu-id="e6e53-120">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="e6e53-121">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6e53-121">EXAMPLES</span></span>

### <span data-ttu-id="e6e53-122">Esempio 1: associare un certificato a un'app Web</span><span class="sxs-lookup"><span data-stu-id="e6e53-122">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com" -CertificatePassword "p@ssw0rd"
```

<span data-ttu-id="e6e53-123">Questo comando associa un certificato Azure esistente (un certificato con l'identificazione personale E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) all'app Web denominata ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="e6e53-123">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

### <span data-ttu-id="e6e53-124">Esempio 2: caricare un certificato e associarlo a un'app Web</span><span class="sxs-lookup"><span data-stu-id="e6e53-124">Example 2: Upload a certificate and bind it to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com" -CertificatePassword "p@ssw0rd" -CertificateFilePath "C:\Certificates\ContosoWebSite.pfx"
```

<span data-ttu-id="e6e53-125">L'esempio 2 associa anche il certificato E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 all'app Web denominata ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="e6e53-125">Example 2 also binds the certificate E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="e6e53-126">In questo caso, tuttavia, il certificato non è stato ancora caricato in Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e53-126">In this case, however, the certificate has not yet been uploaded to Azure.</span></span>
<span data-ttu-id="e6e53-127">Per questo motivo, il parametro *CertificateFilePath* viene usato per specificare la copia locale del certificato. File PFX.</span><span class="sxs-lookup"><span data-stu-id="e6e53-127">Because of that, the *CertificateFilePath* parameter is used to specify the local copy of the certificate .PFX file.</span></span>
<span data-ttu-id="e6e53-128">Questo certificato verrà caricato in Azure e verranno creati i nuovi binding SSL.</span><span class="sxs-lookup"><span data-stu-id="e6e53-128">This certificate will be uploaded to Azure and then the new SSL bindings will be created.</span></span>

## <span data-ttu-id="e6e53-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6e53-129">PARAMETERS</span></span>

### <span data-ttu-id="e6e53-130">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e6e53-130">-CertificateFilePath</span></span>
<span data-ttu-id="e6e53-131">Specifica il percorso del file per il certificato da caricare.</span><span class="sxs-lookup"><span data-stu-id="e6e53-131">Specifies the file path for the certificate to be uploaded.</span></span>

<span data-ttu-id="e6e53-132">Il parametro *CertificateFilePath* è obbligatorio solo se il certificato non è stato ancora caricato in Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e53-132">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

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

### <span data-ttu-id="e6e53-133">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e6e53-133">-CertificatePassword</span></span>
<span data-ttu-id="e6e53-134">Specifica la password di decrittografia per il certificato.</span><span class="sxs-lookup"><span data-stu-id="e6e53-134">Specifies the decryption password for the certificate.</span></span>

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

### <span data-ttu-id="e6e53-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6e53-135">-Name</span></span>
<span data-ttu-id="e6e53-136">Specifica il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="e6e53-136">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="e6e53-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6e53-137">-ResourceGroupName</span></span>
<span data-ttu-id="e6e53-138">Specifica il nome del gruppo di risorse a cui è assegnato il certificato.</span><span class="sxs-lookup"><span data-stu-id="e6e53-138">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="e6e53-139">Non è possibile usare il parametro *ResourceGroupName* e il parametro *Web App* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="e6e53-139">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="e6e53-140">-Slot</span><span class="sxs-lookup"><span data-stu-id="e6e53-140">-Slot</span></span>
<span data-ttu-id="e6e53-141">Specifica il nome dello slot di distribuzione dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="e6e53-141">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="e6e53-142">Puoi usare il cmdlet Get-AzureRMWebAppSlot per ottenere uno slot.</span><span class="sxs-lookup"><span data-stu-id="e6e53-142">You can use the Get-AzureRMWebAppSlot cmdlet to get a slot.</span></span>

<span data-ttu-id="e6e53-143">Gli slot di distribuzione consentono di organizzare e convalidare le app Web senza che le app siano accessibili tramite Internet.</span><span class="sxs-lookup"><span data-stu-id="e6e53-143">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="e6e53-144">In genere, le modifiche verranno distribuite in un sito di staging, convalidarle e quindi distribuirle nel sito di produzione (accessibile tramite Internet).</span><span class="sxs-lookup"><span data-stu-id="e6e53-144">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

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

### <span data-ttu-id="e6e53-145">-SslState</span><span class="sxs-lookup"><span data-stu-id="e6e53-145">-SslState</span></span>
<span data-ttu-id="e6e53-146">Specifica se il certificato è abilitato.</span><span class="sxs-lookup"><span data-stu-id="e6e53-146">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="e6e53-147">Imposta il parametro *SSLState* su 1 per abilitare il certificato oppure imposta *SSLState* su 0 per disabilitare il certificato.</span><span class="sxs-lookup"><span data-stu-id="e6e53-147">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

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

### <span data-ttu-id="e6e53-148">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="e6e53-148">-Thumbprint</span></span>
<span data-ttu-id="e6e53-149">Specifica l'identificatore univoco per il certificato.</span><span class="sxs-lookup"><span data-stu-id="e6e53-149">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="e6e53-150">-Web App</span><span class="sxs-lookup"><span data-stu-id="e6e53-150">-WebApp</span></span>
<span data-ttu-id="e6e53-151">Specifica un'app Web.</span><span class="sxs-lookup"><span data-stu-id="e6e53-151">Specifies a Web App.</span></span>
<span data-ttu-id="e6e53-152">Per ottenere un'app Web, usa il cmdlet Get-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="e6e53-152">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="e6e53-153">Non è possibile usare il parametro *Web App* nello stesso comando del parametro *ResourceGroupName* e/o *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="e6e53-153">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e53-154">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="e6e53-154">-WebAppName</span></span>
<span data-ttu-id="e6e53-155">Specifica il nome dell'app Web per cui è in corso la creazione del nuovo binding SSL.</span><span class="sxs-lookup"><span data-stu-id="e6e53-155">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>

<span data-ttu-id="e6e53-156">Non è possibile usare il parametro *WebAppName* e il parametro *Web App* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="e6e53-156">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="e6e53-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e53-157">-DefaultProfile</span></span>
<span data-ttu-id="e6e53-158">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e53-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6e53-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e53-159">CommonParameters</span></span>
<span data-ttu-id="e6e53-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6e53-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e53-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6e53-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e53-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6e53-162">INPUTS</span></span>

### <span data-ttu-id="e6e53-163">Sito</span><span class="sxs-lookup"><span data-stu-id="e6e53-163">Site</span></span>
<span data-ttu-id="e6e53-164">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e6e53-164">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e6e53-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6e53-165">OUTPUTS</span></span>

## <span data-ttu-id="e6e53-166">Note</span><span class="sxs-lookup"><span data-stu-id="e6e53-166">NOTES</span></span>

## <span data-ttu-id="e6e53-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6e53-167">RELATED LINKS</span></span>

[<span data-ttu-id="e6e53-168">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="e6e53-168">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="e6e53-169">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="e6e53-169">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="e6e53-170">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e6e53-170">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="e6e53-171">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="e6e53-171">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


