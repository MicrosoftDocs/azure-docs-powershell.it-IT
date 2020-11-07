---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
ms.openlocfilehash: de24d9d16af5b429dcf59ffc8f4cbeb7dd0654f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686181"
---
# <span data-ttu-id="28394-101">Remove-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="28394-101">Remove-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="28394-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28394-102">SYNOPSIS</span></span>
<span data-ttu-id="28394-103">Elimina un certificato Hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="28394-103">Deletes an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28394-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28394-104">SYNTAX</span></span>

### <span data-ttu-id="28394-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="28394-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28394-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="28394-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28394-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="28394-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28394-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28394-108">DESCRIPTION</span></span>
<span data-ttu-id="28394-109">Per una spiegazione dettagliata dei certificati della CA in Azure molto Hub, vedere https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="28394-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="28394-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28394-110">EXAMPLES</span></span>

### <span data-ttu-id="28394-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28394-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="28394-112">Elimina il certificato</span><span class="sxs-lookup"><span data-stu-id="28394-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="28394-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28394-113">PARAMETERS</span></span>

### <span data-ttu-id="28394-114">-Certificate</span><span class="sxs-lookup"><span data-stu-id="28394-114">-CertificateName</span></span>
<span data-ttu-id="28394-115">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="28394-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="28394-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28394-116">-DefaultProfile</span></span>
<span data-ttu-id="28394-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28394-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28394-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="28394-118">-Etag</span></span>
<span data-ttu-id="28394-119">ETag del certificato</span><span class="sxs-lookup"><span data-stu-id="28394-119">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28394-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28394-120">-InputObject</span></span>
<span data-ttu-id="28394-121">Oggetto certificato</span><span class="sxs-lookup"><span data-stu-id="28394-121">Certificate Object</span></span>

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

### <span data-ttu-id="28394-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="28394-122">-Name</span></span>
<span data-ttu-id="28394-123">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="28394-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="28394-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28394-124">-PassThru</span></span>
<span data-ttu-id="28394-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="28394-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28394-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28394-126">-ResourceGroupName</span></span>
<span data-ttu-id="28394-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="28394-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="28394-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28394-128">-ResourceId</span></span>
<span data-ttu-id="28394-129">ID risorsa certificato</span><span class="sxs-lookup"><span data-stu-id="28394-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="28394-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="28394-130">-Confirm</span></span>
<span data-ttu-id="28394-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28394-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28394-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28394-132">-WhatIf</span></span>
<span data-ttu-id="28394-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28394-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28394-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28394-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28394-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28394-135">CommonParameters</span></span>
<span data-ttu-id="28394-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28394-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28394-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28394-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28394-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28394-138">INPUTS</span></span>

### <span data-ttu-id="28394-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="28394-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="28394-140">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="28394-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="28394-141">System. String</span><span class="sxs-lookup"><span data-stu-id="28394-141">System.String</span></span>

## <span data-ttu-id="28394-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28394-142">OUTPUTS</span></span>

### <span data-ttu-id="28394-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28394-143">System.Boolean</span></span>

## <span data-ttu-id="28394-144">Note</span><span class="sxs-lookup"><span data-stu-id="28394-144">NOTES</span></span>

## <span data-ttu-id="28394-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28394-145">RELATED LINKS</span></span>
