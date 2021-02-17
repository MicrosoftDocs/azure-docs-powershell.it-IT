---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 6d77bcc6d940c5891b4fc06875dc353af5f75939
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188279"
---
# <span data-ttu-id="4b6ee-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="4b6ee-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="4b6ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b6ee-102">SYNOPSIS</span></span>
<span data-ttu-id="4b6ee-103">Creare/aggiornare un certificato hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b6ee-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="4b6ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b6ee-104">SYNTAX</span></span>

### <span data-ttu-id="4b6ee-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4b6ee-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b6ee-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4b6ee-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b6ee-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4b6ee-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b6ee-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4b6ee-108">DESCRIPTION</span></span>
<span data-ttu-id="4b6ee-109">Carica un nuovo certificato o per sostituire quello esistente con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="4b6ee-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="4b6ee-110">Per una spiegazione dettagliata dei certificati CA nell'Hub IoT di Azure, vedi https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="4b6ee-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="4b6ee-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b6ee-111">EXAMPLES</span></span>

### <span data-ttu-id="4b6ee-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4b6ee-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="4b6ee-113">Carica un file CER del certificato CA in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4b6ee-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="4b6ee-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4b6ee-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="4b6ee-115">Aggiorna un certificato CA in un hub IoT caricando un nuovo file CER.</span><span class="sxs-lookup"><span data-stu-id="4b6ee-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="4b6ee-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b6ee-116">PARAMETERS</span></span>

### <span data-ttu-id="4b6ee-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="4b6ee-117">-CertificateName</span></span>
<span data-ttu-id="4b6ee-118">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="4b6ee-118">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b6ee-119">-DefaultProfile</span></span>
<span data-ttu-id="4b6ee-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b6ee-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b6ee-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="4b6ee-121">-Etag</span></span>
<span data-ttu-id="4b6ee-122">Etag del certificato</span><span class="sxs-lookup"><span data-stu-id="4b6ee-122">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ee-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b6ee-123">-InputObject</span></span>
<span data-ttu-id="4b6ee-124">Oggetto Certificate</span><span class="sxs-lookup"><span data-stu-id="4b6ee-124">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ee-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4b6ee-125">-Name</span></span>
<span data-ttu-id="4b6ee-126">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="4b6ee-126">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ee-127">-Path</span><span class="sxs-lookup"><span data-stu-id="4b6ee-127">-Path</span></span>
<span data-ttu-id="4b6ee-128">Rappresentazione in base 64 del file CON ESTENSIONE CER o PEM del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="4b6ee-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ee-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b6ee-129">-ResourceGroupName</span></span>
<span data-ttu-id="4b6ee-130">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4b6ee-130">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ee-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b6ee-131">-ResourceId</span></span>
<span data-ttu-id="4b6ee-132">ID risorsa certificato</span><span class="sxs-lookup"><span data-stu-id="4b6ee-132">Certificate Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ee-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b6ee-133">-Confirm</span></span>
<span data-ttu-id="4b6ee-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b6ee-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ee-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b6ee-135">-WhatIf</span></span>
<span data-ttu-id="4b6ee-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b6ee-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b6ee-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b6ee-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ee-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b6ee-138">CommonParameters</span></span>
<span data-ttu-id="4b6ee-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b6ee-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b6ee-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b6ee-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b6ee-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="4b6ee-141">INPUTS</span></span>

### <span data-ttu-id="4b6ee-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="4b6ee-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="4b6ee-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4b6ee-143">System.String</span></span>

## <span data-ttu-id="4b6ee-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b6ee-144">OUTPUTS</span></span>

### <span data-ttu-id="4b6ee-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="4b6ee-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="4b6ee-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="4b6ee-146">NOTES</span></span>

## <span data-ttu-id="4b6ee-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b6ee-147">RELATED LINKS</span></span>
