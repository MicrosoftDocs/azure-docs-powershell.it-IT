---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFB0000C-2EFF-4216-923B-55B0B07BFE60
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51ab7d137fbbac1925ae689a1dcb16c89b9b8000
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023564"
---
# <span data-ttu-id="8da5a-101">Get-AzureServiceAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="8da5a-101">Get-AzureServiceAvailableExtension</span></span>

## <span data-ttu-id="8da5a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8da5a-102">SYNOPSIS</span></span>
<span data-ttu-id="8da5a-103">Ottiene informazioni sulle estensioni disponibili per i servizi ospitati.</span><span class="sxs-lookup"><span data-stu-id="8da5a-103">Gets information about the available extensions for hosted services.</span></span>

## <span data-ttu-id="8da5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8da5a-104">SYNTAX</span></span>

### <span data-ttu-id="8da5a-105">ListLatestExtensions (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8da5a-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureServiceAvailableExtension [[-ExtensionName] <String>] [[-ProviderNamespace] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8da5a-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="8da5a-106">ListAllVersions</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8da5a-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="8da5a-107">ListSingleVersion</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8da5a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8da5a-108">DESCRIPTION</span></span>
<span data-ttu-id="8da5a-109">Il cmdlet **Get-AzureServiceAvailableExtension** ottiene informazioni sulle più recenti estensioni disponibili per i servizi ospitati.</span><span class="sxs-lookup"><span data-stu-id="8da5a-109">The **Get-AzureServiceAvailableExtension** cmdlet gets information for the latest available extensions for hosted services.</span></span>

## <span data-ttu-id="8da5a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8da5a-110">EXAMPLES</span></span>

### <span data-ttu-id="8da5a-111">Esempio 1: ottenere le estensioni disponibili</span><span class="sxs-lookup"><span data-stu-id="8da5a-111">Example 1: Get available extensions</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="8da5a-112">Questo comando consente di ottenere tutte le estensioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="8da5a-112">This command gets all available extensions.</span></span>

### <span data-ttu-id="8da5a-113">Esempio 2: ottenere le estensioni in uno spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="8da5a-113">Example 2: Get extensions in a specified namespace</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -AllVersions

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="8da5a-114">Questo comando consente di ottenere le estensioni con un nome specificato in uno spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="8da5a-114">This command gets the extensions with a specified name in a specified namespace.</span></span>

### <span data-ttu-id="8da5a-115">Esempio 3: ottenere una versione specifica di un'estensione</span><span class="sxs-lookup"><span data-stu-id="8da5a-115">Example 3: Get a specific version of an extension</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -Version 1.0.0.1

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="8da5a-116">Questo comando consente di ottenere informazioni su una versione specifica di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="8da5a-116">This command gets information about a specific version of an extension.</span></span>

## <span data-ttu-id="8da5a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8da5a-117">PARAMETERS</span></span>

### <span data-ttu-id="8da5a-118">-AllVersions</span><span class="sxs-lookup"><span data-stu-id="8da5a-118">-AllVersions</span></span>
<span data-ttu-id="8da5a-119">Indica che questo cmdlet ottiene tutte le versioni di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="8da5a-119">Indicates that this cmdlet gets all versions of an extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAllVersions
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da5a-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="8da5a-120">-ExtensionName</span></span>
<span data-ttu-id="8da5a-121">Specifica il nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="8da5a-121">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da5a-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8da5a-122">-InformationAction</span></span>
<span data-ttu-id="8da5a-123">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="8da5a-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8da5a-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8da5a-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8da5a-125">Continuare</span><span class="sxs-lookup"><span data-stu-id="8da5a-125">Continue</span></span>
- <span data-ttu-id="8da5a-126">Ignora</span><span class="sxs-lookup"><span data-stu-id="8da5a-126">Ignore</span></span>
- <span data-ttu-id="8da5a-127">Informarsi</span><span class="sxs-lookup"><span data-stu-id="8da5a-127">Inquire</span></span>
- <span data-ttu-id="8da5a-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8da5a-128">SilentlyContinue</span></span>
- <span data-ttu-id="8da5a-129">Stop</span><span class="sxs-lookup"><span data-stu-id="8da5a-129">Stop</span></span>
- <span data-ttu-id="8da5a-130">Sospensione</span><span class="sxs-lookup"><span data-stu-id="8da5a-130">Suspend</span></span>

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

### <span data-ttu-id="8da5a-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8da5a-131">-InformationVariable</span></span>
<span data-ttu-id="8da5a-132">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="8da5a-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8da5a-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="8da5a-133">-Profile</span></span>
<span data-ttu-id="8da5a-134">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8da5a-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8da5a-135">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8da5a-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8da5a-136">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="8da5a-136">-ProviderNamespace</span></span>
<span data-ttu-id="8da5a-137">Specifica lo spazio dei nomi del provider di estensioni.</span><span class="sxs-lookup"><span data-stu-id="8da5a-137">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da5a-138">-Versione</span><span class="sxs-lookup"><span data-stu-id="8da5a-138">-Version</span></span>
<span data-ttu-id="8da5a-139">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="8da5a-139">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: ListSingleVersion
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da5a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da5a-140">CommonParameters</span></span>
<span data-ttu-id="8da5a-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da5a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da5a-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8da5a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da5a-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8da5a-143">INPUTS</span></span>

## <span data-ttu-id="8da5a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8da5a-144">OUTPUTS</span></span>

## <span data-ttu-id="8da5a-145">Note</span><span class="sxs-lookup"><span data-stu-id="8da5a-145">NOTES</span></span>

## <span data-ttu-id="8da5a-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8da5a-146">RELATED LINKS</span></span>

[<span data-ttu-id="8da5a-147">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="8da5a-147">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)


