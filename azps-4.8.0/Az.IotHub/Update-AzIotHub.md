---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: 3ba9706c452c293dea6ad6a0e23a51ccb03ada9c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189849"
---
# <span data-ttu-id="4be9c-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="4be9c-101">Update-AzIotHub</span></span>

## <span data-ttu-id="4be9c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4be9c-102">SYNOPSIS</span></span>
<span data-ttu-id="4be9c-103">Aggiornare un hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="4be9c-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="4be9c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4be9c-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4be9c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4be9c-105">DESCRIPTION</span></span>
<span data-ttu-id="4be9c-106">Puoi aggiornare le proprietà dei tag di un IotHub.</span><span class="sxs-lookup"><span data-stu-id="4be9c-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="4be9c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4be9c-107">EXAMPLES</span></span>

### <span data-ttu-id="4be9c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4be9c-108">Example 1</span></span>
```
PS C:\> Update-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiotdps
Name           : myiotdps
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[k1, v1]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="4be9c-109">Aggiungi " @tags " al contrassegno di un hub di Azure molto "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="4be9c-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="4be9c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4be9c-110">PARAMETERS</span></span>

### <span data-ttu-id="4be9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be9c-111">-DefaultProfile</span></span>
<span data-ttu-id="4be9c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4be9c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4be9c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4be9c-113">-Name</span></span>
<span data-ttu-id="4be9c-114">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="4be9c-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4be9c-115">-Reset</span><span class="sxs-lookup"><span data-stu-id="4be9c-115">-Reset</span></span>
<span data-ttu-id="4be9c-116">Reimpostare i tag IoTHub</span><span class="sxs-lookup"><span data-stu-id="4be9c-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="4be9c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4be9c-117">-ResourceGroupName</span></span>
<span data-ttu-id="4be9c-118">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4be9c-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4be9c-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="4be9c-119">-Tag</span></span>
<span data-ttu-id="4be9c-120">Raccolta di tag IoTHub</span><span class="sxs-lookup"><span data-stu-id="4be9c-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="4be9c-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4be9c-121">-Confirm</span></span>
<span data-ttu-id="4be9c-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4be9c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4be9c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4be9c-123">-WhatIf</span></span>
<span data-ttu-id="4be9c-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4be9c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4be9c-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4be9c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4be9c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be9c-126">CommonParameters</span></span>
<span data-ttu-id="4be9c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4be9c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be9c-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4be9c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be9c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4be9c-129">INPUTS</span></span>

### <span data-ttu-id="4be9c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4be9c-130">System.String</span></span>

## <span data-ttu-id="4be9c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4be9c-131">OUTPUTS</span></span>

### <span data-ttu-id="4be9c-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4be9c-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="4be9c-133">Note</span><span class="sxs-lookup"><span data-stu-id="4be9c-133">NOTES</span></span>

## <span data-ttu-id="4be9c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4be9c-134">RELATED LINKS</span></span>