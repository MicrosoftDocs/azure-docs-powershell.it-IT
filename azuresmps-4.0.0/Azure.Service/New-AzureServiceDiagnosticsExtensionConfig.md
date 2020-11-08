---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1F76C63E-5289-4F88-9522-3FF4EF732908
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a232ec03da38ea3d527dcd9aa214dbf681bcc6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023856"
---
# <span data-ttu-id="5b892-101">New-AzureServiceDiagnosticsExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="5b892-101">New-AzureServiceDiagnosticsExtensionConfig</span></span>

## <span data-ttu-id="5b892-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b892-102">SYNOPSIS</span></span>
<span data-ttu-id="5b892-103">Genera una configurazione per un'estensione di diagnostica per il ruolo o i ruoli specificati.</span><span class="sxs-lookup"><span data-stu-id="5b892-103">Generates a configuration for a diagnostics extension for specified role(s) or all roles.</span></span>

## <span data-ttu-id="5b892-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b892-104">SYNTAX</span></span>

### <span data-ttu-id="5b892-105">NewExtension (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b892-105">NewExtension (Default)</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5b892-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="5b892-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>]
 [[-StorageContext] <AzureStorageContext>] [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b892-107">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="5b892-107">SetExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5b892-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b892-108">DESCRIPTION</span></span>
<span data-ttu-id="5b892-109">Il cmdlet **New-AzureServiceDiagnosticsExtensionConfig** genera una configurazione per un'estensione di diagnostica per i ruoli specificati o per tutti i ruoli.</span><span class="sxs-lookup"><span data-stu-id="5b892-109">The **New-AzureServiceDiagnosticsExtensionConfig** cmdlet generates a configuration for a diagnostics extension for specified roles or all roles.</span></span>

## <span data-ttu-id="5b892-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b892-110">EXAMPLES</span></span>

### <span data-ttu-id="5b892-111">Esempio 1: creare l'estensione di diagnostica di Azure per tutti i ruoli nel servizio cloud</span><span class="sxs-lookup"><span data-stu-id="5b892-111">Example 1: Create the Azure Diagnostics extension for all roles in the cloud service</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="5b892-112">Questo comando crea l'estensione di diagnostica di Azure per tutti i ruoli nel servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="5b892-112">This command creates the Azure Diagnostics extension for all of the roles in the cloud service.</span></span>

### <span data-ttu-id="5b892-113">Esempio 2: creare l'estensione di diagnostica di Azure per un ruolo</span><span class="sxs-lookup"><span data-stu-id="5b892-113">Example 2: Create the Azure Diagnostics extension for a role</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole1"
```

<span data-ttu-id="5b892-114">Questo comando crea l'estensione di diagnostica di Azure per il ruolo WebRole01 nel servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="5b892-114">This command creates the Azure Diagnostics extension for the role WebRole01 in the cloud service.</span></span>

## <span data-ttu-id="5b892-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b892-115">PARAMETERS</span></span>

### <span data-ttu-id="5b892-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="5b892-116">-CertificateThumbprint</span></span>
<span data-ttu-id="5b892-117">Specifica l'identificazione personale del certificato da usare per crittografare la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="5b892-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="5b892-118">Questo certificato deve essere già presente nell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="5b892-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="5b892-119">Se non si specifica un certificato, questo cmdlet crea un certificato.</span><span class="sxs-lookup"><span data-stu-id="5b892-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b892-120">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="5b892-120">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="5b892-121">Specifica il percorso di configurazione della diagnostica.</span><span class="sxs-lookup"><span data-stu-id="5b892-121">Specifies the diagnostics configuration path.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b892-122">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="5b892-122">-ExtensionId</span></span>
<span data-ttu-id="5b892-123">Specifica l'ID dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="5b892-123">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b892-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5b892-124">-InformationAction</span></span>
<span data-ttu-id="5b892-125">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="5b892-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5b892-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5b892-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5b892-127">Continuare</span><span class="sxs-lookup"><span data-stu-id="5b892-127">Continue</span></span>
- <span data-ttu-id="5b892-128">Ignora</span><span class="sxs-lookup"><span data-stu-id="5b892-128">Ignore</span></span>
- <span data-ttu-id="5b892-129">Informarsi</span><span class="sxs-lookup"><span data-stu-id="5b892-129">Inquire</span></span>
- <span data-ttu-id="5b892-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5b892-130">SilentlyContinue</span></span>
- <span data-ttu-id="5b892-131">Stop</span><span class="sxs-lookup"><span data-stu-id="5b892-131">Stop</span></span>
- <span data-ttu-id="5b892-132">Sospensione</span><span class="sxs-lookup"><span data-stu-id="5b892-132">Suspend</span></span>

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

### <span data-ttu-id="5b892-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5b892-133">-InformationVariable</span></span>
<span data-ttu-id="5b892-134">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="5b892-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5b892-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="5b892-135">-Profile</span></span>
<span data-ttu-id="5b892-136">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b892-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5b892-137">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="5b892-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5b892-138">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="5b892-138">-Role</span></span>
<span data-ttu-id="5b892-139">Specifica una matrice facoltativa di ruoli per specificare la configurazione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="5b892-139">Specifies an optional array of roles to specify the diagnostics configuration for.</span></span>
<span data-ttu-id="5b892-140">Se non è specificata, la configurazione di diagnostica viene applicata come configurazione predefinita per tutti i ruoli.</span><span class="sxs-lookup"><span data-stu-id="5b892-140">If not specified the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b892-141">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b892-141">-StorageAccountEndpoint</span></span>
<span data-ttu-id="5b892-142">Specifica l'endpoint dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5b892-142">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b892-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5b892-143">-StorageAccountKey</span></span>
<span data-ttu-id="5b892-144">Specifica la chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5b892-144">Specifies the storage account key.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b892-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5b892-145">-StorageAccountName</span></span>
<span data-ttu-id="5b892-146">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5b892-146">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b892-147">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="5b892-147">-StorageContext</span></span>
<span data-ttu-id="5b892-148">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5b892-148">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b892-149">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="5b892-149">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="5b892-150">Specifica un algoritmo di hash dell'identificazione digitale usato con l'identificazione personale per identificare il certificato.</span><span class="sxs-lookup"><span data-stu-id="5b892-150">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="5b892-151">Questo parametro è facoltativo e il valore predefinito è SHA1.</span><span class="sxs-lookup"><span data-stu-id="5b892-151">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b892-152">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="5b892-152">-X509Certificate</span></span>
<span data-ttu-id="5b892-153">Specifica un certificato X. 509 caricato automaticamente nel servizio cloud e usato per crittografare la configurazione privata dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="5b892-153">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: NewExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b892-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b892-154">CommonParameters</span></span>
<span data-ttu-id="5b892-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b892-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b892-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b892-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b892-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b892-157">INPUTS</span></span>

## <span data-ttu-id="5b892-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b892-158">OUTPUTS</span></span>

## <span data-ttu-id="5b892-159">Note</span><span class="sxs-lookup"><span data-stu-id="5b892-159">NOTES</span></span>

## <span data-ttu-id="5b892-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b892-160">RELATED LINKS</span></span>

[<span data-ttu-id="5b892-161">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5b892-161">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="5b892-162">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5b892-162">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


