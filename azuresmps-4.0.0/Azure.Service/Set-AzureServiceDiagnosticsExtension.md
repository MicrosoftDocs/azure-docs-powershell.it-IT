---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2E738CEF-BBDD-425D-B12C-86FF7C45A634
online version: ''
schema: 2.0.0
ms.openlocfilehash: 518528d4af8889cf36b30c417e0170e0ea228ebf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029509"
---
# <span data-ttu-id="1ac01-101">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1ac01-101">Set-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="1ac01-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ac01-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac01-103">Abilita l'estensione di diagnostica di Azure nei ruoli specificati o in tutti i ruoli in un servizio distribuito o alla distribuzione.</span><span class="sxs-lookup"><span data-stu-id="1ac01-103">Enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="1ac01-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ac01-104">SYNTAX</span></span>

### <span data-ttu-id="1ac01-105">Seextension (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1ac01-105">SetExtension (Default)</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ac01-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="1ac01-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-CertificateThumbprint] <String>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1ac01-107">SetExtensionUsingDiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ac01-107">SetExtensionUsingDiagnosticsConfiguration</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-DiagnosticsConfiguration] <ExtensionConfigurationInput[]> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1ac01-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ac01-108">DESCRIPTION</span></span>
<span data-ttu-id="1ac01-109">Il cmdlet **set-AzureServiceDiagnosticsExtension** Abilita l'estensione di Azure Diagnostics nei ruoli specificati o in tutti i ruoli in un servizio distribuito o alla distribuzione.</span><span class="sxs-lookup"><span data-stu-id="1ac01-109">The **Set-AzureServiceDiagnosticsExtension** cmdlet enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="1ac01-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ac01-110">EXAMPLES</span></span>

### <span data-ttu-id="1ac01-111">Esempio 1: Enable Azure Diagnostics Extension</span><span class="sxs-lookup"><span data-stu-id="1ac01-111">Example 1: Enable Azure Diagnostics extension</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="1ac01-112">Questo comando Abilita l'estensione di diagnostica di Azure per tutti i ruoli.</span><span class="sxs-lookup"><span data-stu-id="1ac01-112">This command enables the Azure Diagnostics extension for all roles.</span></span>

### <span data-ttu-id="1ac01-113">Esempio 2: abilitare l'estensione di diagnostica Azure per un ruolo specificato</span><span class="sxs-lookup"><span data-stu-id="1ac01-113">Example 2: Enable Azure Diagnostics extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole01"
```

<span data-ttu-id="1ac01-114">Questo comando Abilita l'estensione di diagnostica di Azure per un ruolo specificato.</span><span class="sxs-lookup"><span data-stu-id="1ac01-114">This command enables the Azure Diagnostics extension for a specified role.</span></span>

## <span data-ttu-id="1ac01-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ac01-115">PARAMETERS</span></span>

### <span data-ttu-id="1ac01-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="1ac01-116">-CertificateThumbprint</span></span>
<span data-ttu-id="1ac01-117">Specifica l'identificazione personale del certificato da usare per crittografare la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="1ac01-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="1ac01-118">Questo certificato deve essere già presente nell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="1ac01-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="1ac01-119">Se non si specifica un certificato, questo cmdlet crea un certificato.</span><span class="sxs-lookup"><span data-stu-id="1ac01-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac01-120">-DiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ac01-120">-DiagnosticsConfiguration</span></span>
<span data-ttu-id="1ac01-121">Specifica una matrice di configurazione per la diagnostica Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac01-121">Specifies an array of configuration for Azure Diagnostics.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: SetExtensionUsingDiagnosticsConfiguration
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac01-122">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="1ac01-122">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="1ac01-123">Specifica la configurazione per la diagnostica Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac01-123">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="1ac01-124">Per scaricare lo schema, è possibile usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="1ac01-124">You can download the schema by using the following command:</span></span> 

`(Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'`

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac01-125">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="1ac01-125">-ExtensionId</span></span>
<span data-ttu-id="1ac01-126">Specifica l'ID di estensione</span><span class="sxs-lookup"><span data-stu-id="1ac01-126">Specifies the extension ID</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac01-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1ac01-127">-InformationAction</span></span>
<span data-ttu-id="1ac01-128">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="1ac01-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1ac01-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1ac01-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1ac01-130">Continuare</span><span class="sxs-lookup"><span data-stu-id="1ac01-130">Continue</span></span>
- <span data-ttu-id="1ac01-131">Ignora</span><span class="sxs-lookup"><span data-stu-id="1ac01-131">Ignore</span></span>
- <span data-ttu-id="1ac01-132">Informarsi</span><span class="sxs-lookup"><span data-stu-id="1ac01-132">Inquire</span></span>
- <span data-ttu-id="1ac01-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1ac01-133">SilentlyContinue</span></span>
- <span data-ttu-id="1ac01-134">Stop</span><span class="sxs-lookup"><span data-stu-id="1ac01-134">Stop</span></span>
- <span data-ttu-id="1ac01-135">Sospensione</span><span class="sxs-lookup"><span data-stu-id="1ac01-135">Suspend</span></span>

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

### <span data-ttu-id="1ac01-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1ac01-136">-InformationVariable</span></span>
<span data-ttu-id="1ac01-137">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="1ac01-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1ac01-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="1ac01-138">-Profile</span></span>
<span data-ttu-id="1ac01-139">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ac01-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1ac01-140">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1ac01-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1ac01-141">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="1ac01-141">-Role</span></span>
<span data-ttu-id="1ac01-142">Specifica una matrice facoltativa di ruoli per cui specificare la configurazione di Azure Diagnostics.</span><span class="sxs-lookup"><span data-stu-id="1ac01-142">Specifies an optional array of roles for which to specify the Azure Diagnostics configuration.</span></span>
<span data-ttu-id="1ac01-143">Se non specifichi questo parametro, la configurazione di diagnostica viene applicata come configurazione predefinita per tutti i ruoli.</span><span class="sxs-lookup"><span data-stu-id="1ac01-143">If you do not specify this parameter, the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac01-144">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1ac01-144">-ServiceName</span></span>
<span data-ttu-id="1ac01-145">Specifica il nome del servizio Azure della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="1ac01-145">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="1ac01-146">-Slot</span><span class="sxs-lookup"><span data-stu-id="1ac01-146">-Slot</span></span>
<span data-ttu-id="1ac01-147">Specifica l'ambiente della distribuzione da modificare.</span><span class="sxs-lookup"><span data-stu-id="1ac01-147">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="1ac01-148">I valori accettabili per questo parametro sono: produzione o staging.</span><span class="sxs-lookup"><span data-stu-id="1ac01-148">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="1ac01-149">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ac01-149">-StorageAccountEndpoint</span></span>
<span data-ttu-id="1ac01-150">Specifica un endpoint dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1ac01-150">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac01-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1ac01-151">-StorageAccountKey</span></span>
<span data-ttu-id="1ac01-152">Specifica una chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1ac01-152">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac01-153">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1ac01-153">-StorageAccountName</span></span>
<span data-ttu-id="1ac01-154">Specifica un nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1ac01-154">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac01-155">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="1ac01-155">-StorageContext</span></span>
<span data-ttu-id="1ac01-156">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac01-156">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac01-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="1ac01-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="1ac01-158">Specifica un algoritmo di hash dell'identificazione digitale usato con l'identificazione personale per identificare il certificato.</span><span class="sxs-lookup"><span data-stu-id="1ac01-158">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="1ac01-159">Questo parametro è facoltativo e il valore predefinito è SHA1.</span><span class="sxs-lookup"><span data-stu-id="1ac01-159">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac01-160">-Versione</span><span class="sxs-lookup"><span data-stu-id="1ac01-160">-Version</span></span>
<span data-ttu-id="1ac01-161">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="1ac01-161">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac01-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="1ac01-162">-X509Certificate</span></span>
<span data-ttu-id="1ac01-163">Specifica un certificato X. 509 che, se specificato, viene caricato automaticamente nel servizio cloud e usato per crittografare la configurazione privata dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="1ac01-163">Specifies an X.509 certificate that, when specified, is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="1ac01-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac01-164">CommonParameters</span></span>
<span data-ttu-id="1ac01-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ac01-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac01-166">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ac01-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac01-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ac01-167">INPUTS</span></span>

## <span data-ttu-id="1ac01-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ac01-168">OUTPUTS</span></span>

## <span data-ttu-id="1ac01-169">Note</span><span class="sxs-lookup"><span data-stu-id="1ac01-169">NOTES</span></span>

## <span data-ttu-id="1ac01-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ac01-170">RELATED LINKS</span></span>

[<span data-ttu-id="1ac01-171">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1ac01-171">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="1ac01-172">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1ac01-172">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)


