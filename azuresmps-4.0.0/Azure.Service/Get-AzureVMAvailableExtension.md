---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAC3DABB-8230-4E86-9936-0F1848980EA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: d062b4300af2efbd45bfccd7ed467871b23d8256
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030006"
---
# <span data-ttu-id="39987-101">Get-AzureVMAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="39987-101">Get-AzureVMAvailableExtension</span></span>

## <span data-ttu-id="39987-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39987-102">SYNOPSIS</span></span>
<span data-ttu-id="39987-103">Ottiene informazioni sulle più recenti estensioni disponibili per le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="39987-103">Gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="39987-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39987-104">SYNTAX</span></span>

### <span data-ttu-id="39987-105">ListLatestExtensions (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39987-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureVMAvailableExtension [[-ExtensionName] <String>] [[-Publisher] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="39987-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="39987-106">ListAllVersions</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="39987-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="39987-107">ListSingleVersion</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="39987-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39987-108">DESCRIPTION</span></span>
<span data-ttu-id="39987-109">Il cmdlet **Get-AzureVMAvailableExtension** ottiene informazioni sulle più recenti estensioni disponibili per le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="39987-109">The **Get-AzureVMAvailableExtension** cmdlet gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="39987-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39987-110">EXAMPLES</span></span>

### <span data-ttu-id="39987-111">Esempio 1: ottenere informazioni sulle più recenti estensioni disponibili</span><span class="sxs-lookup"><span data-stu-id="39987-111">Example 1: Get information for the latest available extensions</span></span>
```
PS C:\> Get-AzureVMAvailableExtension
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="39987-112">Questo comando consente di ottenere informazioni sulle più recenti estensioni disponibili per tutte le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="39987-112">This command gets information for the latest available extensions for all virtual machines.</span></span>

### <span data-ttu-id="39987-113">Esempio 2: ottenere informazioni da un nome di estensione specificato</span><span class="sxs-lookup"><span data-stu-id="39987-113">Example 2: Get information from a specified extension name</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName "VMAccessAgent" -AllVersions
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.2
          PublicConfigurationSchema  : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          PrivateConfigurationSchema : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded

          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="39987-114">Questo comando consente di ottenere informazioni da tutte le versioni dell'estensione denominate VMAccessAgent e dal server di pubblicazione denominato Microsoft. computer.</span><span class="sxs-lookup"><span data-stu-id="39987-114">This command gets information from all versions of the extension named VMAccessAgent and the publisher named Microsoft.Computer.</span></span>

### <span data-ttu-id="39987-115">Esempio 3: ottenere informazioni da una specifica estensione di una macchina virtuale in base al numero di versione</span><span class="sxs-lookup"><span data-stu-id="39987-115">Example 3: Get information from a specific virtual machine extension by version number</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName VMAccessAgent -Version 1.0.3
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="39987-116">Questo comando ottiene le informazioni per l'estensione denominata VMAccessAgent e il server di pubblicazione denominato Microsoft. COMPUTE per l'estensione della versione 1.0.3.</span><span class="sxs-lookup"><span data-stu-id="39987-116">This command gets information for the extension named VMAccessAgent and the publisher named Microsoft.Compute for the extension version 1.0.3.</span></span>

## <span data-ttu-id="39987-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39987-117">PARAMETERS</span></span>

### <span data-ttu-id="39987-118">-AllVersions</span><span class="sxs-lookup"><span data-stu-id="39987-118">-AllVersions</span></span>
<span data-ttu-id="39987-119">Indica che questo cmdlet elenca tutte le versioni di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="39987-119">Indicates that this cmdlet lists all versions of an extension.</span></span>

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

### <span data-ttu-id="39987-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="39987-120">-ExtensionName</span></span>
<span data-ttu-id="39987-121">Specifica il nome dell'estensione disponibile.</span><span class="sxs-lookup"><span data-stu-id="39987-121">Specifies the name of the available extension.</span></span>

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

### <span data-ttu-id="39987-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="39987-122">-InformationAction</span></span>
<span data-ttu-id="39987-123">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="39987-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="39987-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="39987-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="39987-125">Continuare</span><span class="sxs-lookup"><span data-stu-id="39987-125">Continue</span></span>
- <span data-ttu-id="39987-126">Ignora</span><span class="sxs-lookup"><span data-stu-id="39987-126">Ignore</span></span>
- <span data-ttu-id="39987-127">Informarsi</span><span class="sxs-lookup"><span data-stu-id="39987-127">Inquire</span></span>
- <span data-ttu-id="39987-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="39987-128">SilentlyContinue</span></span>
- <span data-ttu-id="39987-129">Stop</span><span class="sxs-lookup"><span data-stu-id="39987-129">Stop</span></span>
- <span data-ttu-id="39987-130">Sospensione</span><span class="sxs-lookup"><span data-stu-id="39987-130">Suspend</span></span>

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

### <span data-ttu-id="39987-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="39987-131">-InformationVariable</span></span>
<span data-ttu-id="39987-132">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="39987-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="39987-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="39987-133">-Profile</span></span>
<span data-ttu-id="39987-134">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39987-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="39987-135">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="39987-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="39987-136">-Publisher</span><span class="sxs-lookup"><span data-stu-id="39987-136">-Publisher</span></span>
<span data-ttu-id="39987-137">Specifica l'editore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="39987-137">Specifies the publisher of the extension.</span></span>

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

### <span data-ttu-id="39987-138">-Versione</span><span class="sxs-lookup"><span data-stu-id="39987-138">-Version</span></span>
<span data-ttu-id="39987-139">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="39987-139">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="39987-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39987-140">CommonParameters</span></span>
<span data-ttu-id="39987-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39987-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39987-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39987-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39987-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39987-143">INPUTS</span></span>

## <span data-ttu-id="39987-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39987-144">OUTPUTS</span></span>

## <span data-ttu-id="39987-145">Note</span><span class="sxs-lookup"><span data-stu-id="39987-145">NOTES</span></span>

## <span data-ttu-id="39987-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39987-146">RELATED LINKS</span></span>

