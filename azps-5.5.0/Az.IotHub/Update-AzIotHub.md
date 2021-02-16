---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: fce61fd015271c9f6b5a3752fae33eaa80d6447c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185598"
---
# <span data-ttu-id="4069d-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="4069d-101">Update-AzIotHub</span></span>

## <span data-ttu-id="4069d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4069d-102">SYNOPSIS</span></span>
<span data-ttu-id="4069d-103">Aggiornare un Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="4069d-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="4069d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4069d-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4069d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4069d-105">DESCRIPTION</span></span>
<span data-ttu-id="4069d-106">È possibile aggiornare le proprietà dei tag di iotHub.</span><span class="sxs-lookup"><span data-stu-id="4069d-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="4069d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4069d-107">EXAMPLES</span></span>

### <span data-ttu-id="4069d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4069d-108">Example 1</span></span>
```
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> Update-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -Tag $updatedTag

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiothub
Name           : myiothub
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[key0, value0]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="4069d-109">Aggiornare i tag di un Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4069d-109">Update tags of an IoT Hub.</span></span>

## <span data-ttu-id="4069d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4069d-110">PARAMETERS</span></span>

### <span data-ttu-id="4069d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4069d-111">-DefaultProfile</span></span>
<span data-ttu-id="4069d-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4069d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4069d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4069d-113">-Name</span></span>
<span data-ttu-id="4069d-114">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="4069d-114">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4069d-115">-Reimposta</span><span class="sxs-lookup"><span data-stu-id="4069d-115">-Reset</span></span>
<span data-ttu-id="4069d-116">Reimpostare tag di IoTHub</span><span class="sxs-lookup"><span data-stu-id="4069d-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="4069d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4069d-117">-ResourceGroupName</span></span>
<span data-ttu-id="4069d-118">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4069d-118">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4069d-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="4069d-119">-Tag</span></span>
<span data-ttu-id="4069d-120">Raccolta di tag IoTHub</span><span class="sxs-lookup"><span data-stu-id="4069d-120">IoTHub Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4069d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4069d-121">-Confirm</span></span>
<span data-ttu-id="4069d-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4069d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4069d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4069d-123">-WhatIf</span></span>
<span data-ttu-id="4069d-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4069d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4069d-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4069d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4069d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4069d-126">CommonParameters</span></span>
<span data-ttu-id="4069d-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4069d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4069d-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4069d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4069d-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="4069d-129">INPUTS</span></span>

### <span data-ttu-id="4069d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4069d-130">System.String</span></span>

## <span data-ttu-id="4069d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4069d-131">OUTPUTS</span></span>

### <span data-ttu-id="4069d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4069d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="4069d-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="4069d-133">NOTES</span></span>

## <span data-ttu-id="4069d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4069d-134">RELATED LINKS</span></span>
