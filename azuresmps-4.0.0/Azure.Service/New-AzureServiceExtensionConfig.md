---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E27283AF-4057-48D9-9F08-7D36290DD907
online version: ''
schema: 2.0.0
ms.openlocfilehash: dfe55fb2ced2275eae06e96480249acd99d3ad6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023854"
---
# <span data-ttu-id="6411e-101">New-AzureServiceExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="6411e-101">New-AzureServiceExtensionConfig</span></span>

## <span data-ttu-id="6411e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6411e-102">SYNOPSIS</span></span>
<span data-ttu-id="6411e-103">Crea una configurazione dell'estensione del servizio cloud per una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6411e-103">Creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="6411e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6411e-104">SYNTAX</span></span>

### <span data-ttu-id="6411e-105">NewExtension (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6411e-105">NewExtension (Default)</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6411e-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="6411e-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6411e-107">UpdateExtensionStatusParameterSetName</span><span class="sxs-lookup"><span data-stu-id="6411e-107">UpdateExtensionStatusParameterSetName</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-ExtensionId] <String> [-ExtensionState] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="6411e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6411e-108">DESCRIPTION</span></span>
<span data-ttu-id="6411e-109">Il cmdlet **New-AzureServiceExtensionConfig** crea una configurazione dell'estensione del servizio cloud per una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6411e-109">The **New-AzureServiceExtensionConfig** cmdlet creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="6411e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6411e-110">EXAMPLES</span></span>

### <span data-ttu-id="6411e-111">Esempio 1: creare una configurazione di estensione</span><span class="sxs-lookup"><span data-stu-id="6411e-111">Example 1: Create an extension configuration</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -ExtensionName 'RDP' -Version '1.0' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="6411e-112">Questo comando specifica una configurazione di estensione.</span><span class="sxs-lookup"><span data-stu-id="6411e-112">This command specifies an extension configuration.</span></span>

### <span data-ttu-id="6411e-113">Esempio 2: creare una configurazione di estensione per un ruolo</span><span class="sxs-lookup"><span data-stu-id="6411e-113">Example 2: Create an extension configuration for a role</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -Role WebRole1 -ExtensionName 'RDP' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="6411e-114">Questo comando specifica una configurazione di estensione per il ruolo WebRole1.</span><span class="sxs-lookup"><span data-stu-id="6411e-114">This command specifies an extension configuration for the role WebRole1.</span></span>

## <span data-ttu-id="6411e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6411e-115">PARAMETERS</span></span>

### <span data-ttu-id="6411e-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="6411e-116">-CertificateThumbprint</span></span>
<span data-ttu-id="6411e-117">Specifica l'identificazione personale del certificato da usare per crittografare la configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="6411e-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="6411e-118">Questo certificato deve essere già presente nell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="6411e-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="6411e-119">Se non si specifica un certificato, questo cmdlet crea un certificato.</span><span class="sxs-lookup"><span data-stu-id="6411e-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="6411e-120">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="6411e-120">-ExtensionId</span></span>
<span data-ttu-id="6411e-121">Specifica il nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="6411e-121">Specifies the name of the extension.</span></span>

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

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6411e-122">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="6411e-122">-ExtensionName</span></span>
<span data-ttu-id="6411e-123">Specifica il nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="6411e-123">Specifies the name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6411e-124">-ExtensionState</span><span class="sxs-lookup"><span data-stu-id="6411e-124">-ExtensionState</span></span>
<span data-ttu-id="6411e-125">Specifica lo stato dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="6411e-125">Specifies the state of the extension.</span></span>
<span data-ttu-id="6411e-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6411e-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6411e-127">Abilita</span><span class="sxs-lookup"><span data-stu-id="6411e-127">Enable</span></span> 
- <span data-ttu-id="6411e-128">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="6411e-128">Disable</span></span> 
- <span data-ttu-id="6411e-129">Disinstallare</span><span class="sxs-lookup"><span data-stu-id="6411e-129">Uninstall</span></span>

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6411e-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6411e-130">-InformationAction</span></span>
<span data-ttu-id="6411e-131">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="6411e-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6411e-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6411e-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6411e-133">Continuare</span><span class="sxs-lookup"><span data-stu-id="6411e-133">Continue</span></span>
- <span data-ttu-id="6411e-134">Ignora</span><span class="sxs-lookup"><span data-stu-id="6411e-134">Ignore</span></span>
- <span data-ttu-id="6411e-135">Informarsi</span><span class="sxs-lookup"><span data-stu-id="6411e-135">Inquire</span></span>
- <span data-ttu-id="6411e-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6411e-136">SilentlyContinue</span></span>
- <span data-ttu-id="6411e-137">Stop</span><span class="sxs-lookup"><span data-stu-id="6411e-137">Stop</span></span>
- <span data-ttu-id="6411e-138">Sospensione</span><span class="sxs-lookup"><span data-stu-id="6411e-138">Suspend</span></span>

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

### <span data-ttu-id="6411e-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6411e-139">-InformationVariable</span></span>
<span data-ttu-id="6411e-140">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="6411e-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6411e-141">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="6411e-141">-PrivateConfiguration</span></span>
<span data-ttu-id="6411e-142">Specifica il testo della configurazione privata.</span><span class="sxs-lookup"><span data-stu-id="6411e-142">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6411e-143">-Profile</span><span class="sxs-lookup"><span data-stu-id="6411e-143">-Profile</span></span>
<span data-ttu-id="6411e-144">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6411e-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6411e-145">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="6411e-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6411e-146">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="6411e-146">-ProviderNamespace</span></span>
<span data-ttu-id="6411e-147">Specifica lo spazio dei nomi provider dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="6411e-147">Specifies the Extension's Provider Namespace.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6411e-148">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="6411e-148">-PublicConfiguration</span></span>
<span data-ttu-id="6411e-149">Specifica il testo della configurazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="6411e-149">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6411e-150">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="6411e-150">-Role</span></span>
<span data-ttu-id="6411e-151">Specifica una matrice facoltativa di ruoli per specificare la configurazione desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="6411e-151">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="6411e-152">Se non è specificata, la configurazione desktop remoto viene applicata come configurazione predefinita per tutti i ruoli.</span><span class="sxs-lookup"><span data-stu-id="6411e-152">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6411e-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="6411e-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="6411e-154">Specifica un algoritmo di hash dell'identificazione digitale usato con l'identificazione personale per identificare il certificato.</span><span class="sxs-lookup"><span data-stu-id="6411e-154">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="6411e-155">Questo parametro è facoltativo e il valore predefinito è SHA1.</span><span class="sxs-lookup"><span data-stu-id="6411e-155">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="6411e-156">-Versione</span><span class="sxs-lookup"><span data-stu-id="6411e-156">-Version</span></span>
<span data-ttu-id="6411e-157">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="6411e-157">Specifies the extension version.</span></span>

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

### <span data-ttu-id="6411e-158">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="6411e-158">-X509Certificate</span></span>
<span data-ttu-id="6411e-159">Specifica un certificato X509 che, se specificato, verrà caricato automaticamente nel servizio cloud e usato per crittografare la configurazione privata dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="6411e-159">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="6411e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6411e-160">CommonParameters</span></span>
<span data-ttu-id="6411e-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6411e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6411e-162">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6411e-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6411e-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6411e-163">INPUTS</span></span>

## <span data-ttu-id="6411e-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6411e-164">OUTPUTS</span></span>

## <span data-ttu-id="6411e-165">Note</span><span class="sxs-lookup"><span data-stu-id="6411e-165">NOTES</span></span>

## <span data-ttu-id="6411e-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6411e-166">RELATED LINKS</span></span>

[<span data-ttu-id="6411e-167">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="6411e-167">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="6411e-168">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="6411e-168">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


