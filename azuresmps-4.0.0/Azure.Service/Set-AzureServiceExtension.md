---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D37920D3-AF6C-4CFC-B9A3-8ED931AEC0DC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 318683c26d05c624549363ff1afe4a2b963c1fe6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023405"
---
# <span data-ttu-id="404e0-101">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="404e0-101">Set-AzureServiceExtension</span></span>

## <span data-ttu-id="404e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="404e0-102">SYNOPSIS</span></span>
<span data-ttu-id="404e0-103">Aggiunge un'estensione del servizio cloud a una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="404e0-103">Adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="404e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="404e0-104">SYNTAX</span></span>

### <span data-ttu-id="404e0-105">Seextension (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="404e0-105">SetExtension (Default)</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="404e0-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="404e0-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="404e0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="404e0-107">DESCRIPTION</span></span>
<span data-ttu-id="404e0-108">Il cmdlet **set-AzureServiceExtension** aggiunge un'estensione del servizio cloud a una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="404e0-108">The **Set-AzureServiceExtension** cmdlet adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="404e0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="404e0-109">EXAMPLES</span></span>

### <span data-ttu-id="404e0-110">Esempio 1: aggiungere un servizio cloud a una distribuzione</span><span class="sxs-lookup"><span data-stu-id="404e0-110">Example 1: Add a cloud service to a deployment</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -ExtensionName "RDP" -Version "1.0" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="404e0-111">Questo comando aggiunge un servizio cloud a una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="404e0-111">This command adds a cloud service to a deployment.</span></span>

### <span data-ttu-id="404e0-112">Esempio 2: aggiungere un servizio cloud a una distribuzione per un ruolo specificato</span><span class="sxs-lookup"><span data-stu-id="404e0-112">Example 2: Add a cloud service to a deployment for a specified role</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -Role "WebRole1" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="404e0-113">Questo comando aggiunge un servizio cloud a una distribuzione per un ruolo specificato.</span><span class="sxs-lookup"><span data-stu-id="404e0-113">This command adds a cloud service to a deployment for a specified role.</span></span>

## <span data-ttu-id="404e0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="404e0-114">PARAMETERS</span></span>

### <span data-ttu-id="404e0-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="404e0-115">-CertificateThumbprint</span></span>
<span data-ttu-id="404e0-116">Specifica l'identificazione personale del certificato da usare per crittografare la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="404e0-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="404e0-117">Questo certificato deve essere già presente nell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="404e0-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="404e0-118">Se non si specifica un certificato, questo cmdlet crea un certificato.</span><span class="sxs-lookup"><span data-stu-id="404e0-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404e0-119">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="404e0-119">-ExtensionId</span></span>
<span data-ttu-id="404e0-120">Specifica l'ID dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="404e0-120">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404e0-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="404e0-121">-ExtensionName</span></span>
<span data-ttu-id="404e0-122">Specifica il nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="404e0-122">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404e0-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="404e0-123">-InformationAction</span></span>
<span data-ttu-id="404e0-124">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="404e0-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="404e0-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="404e0-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="404e0-126">Continuare</span><span class="sxs-lookup"><span data-stu-id="404e0-126">Continue</span></span>
- <span data-ttu-id="404e0-127">Ignora</span><span class="sxs-lookup"><span data-stu-id="404e0-127">Ignore</span></span>
- <span data-ttu-id="404e0-128">Informarsi</span><span class="sxs-lookup"><span data-stu-id="404e0-128">Inquire</span></span>
- <span data-ttu-id="404e0-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="404e0-129">SilentlyContinue</span></span>
- <span data-ttu-id="404e0-130">Stop</span><span class="sxs-lookup"><span data-stu-id="404e0-130">Stop</span></span>
- <span data-ttu-id="404e0-131">Sospensione</span><span class="sxs-lookup"><span data-stu-id="404e0-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404e0-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="404e0-132">-InformationVariable</span></span>
<span data-ttu-id="404e0-133">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="404e0-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404e0-134">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="404e0-134">-PrivateConfiguration</span></span>
<span data-ttu-id="404e0-135">Specifica il testo della configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="404e0-135">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404e0-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="404e0-136">-Profile</span></span>
<span data-ttu-id="404e0-137">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="404e0-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="404e0-138">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="404e0-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404e0-139">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="404e0-139">-ProviderNamespace</span></span>
<span data-ttu-id="404e0-140">Specifica lo spazio dei nomi del provider di estensioni.</span><span class="sxs-lookup"><span data-stu-id="404e0-140">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404e0-141">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="404e0-141">-PublicConfiguration</span></span>
<span data-ttu-id="404e0-142">Specifica il testo della configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="404e0-142">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404e0-143">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="404e0-143">-Role</span></span>
<span data-ttu-id="404e0-144">Specifica una matrice facoltativa di ruoli per cui specificare la configurazione desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="404e0-144">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="404e0-145">Se questo parametro non viene specificato, la configurazione desktop remoto viene applicata come configurazione predefinita per tutti i ruoli.</span><span class="sxs-lookup"><span data-stu-id="404e0-145">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404e0-146">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="404e0-146">-ServiceName</span></span>
<span data-ttu-id="404e0-147">Specifica il nome del servizio Azure della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="404e0-147">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404e0-148">-Slot</span><span class="sxs-lookup"><span data-stu-id="404e0-148">-Slot</span></span>
<span data-ttu-id="404e0-149">Specifica l'ambiente della distribuzione da modificare.</span><span class="sxs-lookup"><span data-stu-id="404e0-149">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="404e0-150">I valori validi sono: produzione o staging.</span><span class="sxs-lookup"><span data-stu-id="404e0-150">Valid values are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404e0-151">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="404e0-151">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="404e0-152">Specifica l'algoritmo di hash delle identificazioni personali usato con l'identificazione personale per identificare il certificato.</span><span class="sxs-lookup"><span data-stu-id="404e0-152">Specifies the thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="404e0-153">Questo parametro è facoltativo e il valore predefinito è SHA1.</span><span class="sxs-lookup"><span data-stu-id="404e0-153">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404e0-154">-Versione</span><span class="sxs-lookup"><span data-stu-id="404e0-154">-Version</span></span>
<span data-ttu-id="404e0-155">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="404e0-155">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404e0-156">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="404e0-156">-X509Certificate</span></span>
<span data-ttu-id="404e0-157">Specifica un certificato X. 509 caricato automaticamente nel servizio cloud e usato per crittografare la configurazione privata dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="404e0-157">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: SetExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404e0-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="404e0-158">CommonParameters</span></span>
<span data-ttu-id="404e0-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="404e0-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="404e0-160">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="404e0-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="404e0-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="404e0-161">INPUTS</span></span>

## <span data-ttu-id="404e0-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="404e0-162">OUTPUTS</span></span>

## <span data-ttu-id="404e0-163">Note</span><span class="sxs-lookup"><span data-stu-id="404e0-163">NOTES</span></span>

## <span data-ttu-id="404e0-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="404e0-164">RELATED LINKS</span></span>

[<span data-ttu-id="404e0-165">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="404e0-165">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="404e0-166">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="404e0-166">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)


