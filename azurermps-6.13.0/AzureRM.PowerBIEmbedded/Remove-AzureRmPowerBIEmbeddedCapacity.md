---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: c2dc0333d2e991b21ac1a921465971f2131f5c3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519240"
---
# <span data-ttu-id="e02ab-101">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e02ab-101">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e02ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e02ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e02ab-103">Elimina un'istanza della capacità incorporata di PowerBI.</span><span class="sxs-lookup"><span data-stu-id="e02ab-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e02ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e02ab-104">SYNTAX</span></span>

### <span data-ttu-id="e02ab-105">ByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e02ab-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e02ab-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e02ab-106">ByResourceId</span></span>
```
Remove-AzureRmPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e02ab-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e02ab-107">ByInputObject</span></span>
```
Remove-AzureRmPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e02ab-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e02ab-108">DESCRIPTION</span></span>
<span data-ttu-id="e02ab-109">Il cmdlet Remove-AzureRmPowerBIEmbeddedCapacity Elimina un'istanza della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="e02ab-109">The Remove-AzureRmPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="e02ab-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e02ab-110">EXAMPLES</span></span>

### <span data-ttu-id="e02ab-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e02ab-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="e02ab-112">Questo comando rimuoverà la capacità denominata testcapacity nel ResourceGroup testRG</span><span class="sxs-lookup"><span data-stu-id="e02ab-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="e02ab-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e02ab-113">PARAMETERS</span></span>

### <span data-ttu-id="e02ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02ab-114">-DefaultProfile</span></span>
<span data-ttu-id="e02ab-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e02ab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e02ab-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e02ab-116">-InputObject</span></span>
<span data-ttu-id="e02ab-117">Oggetto di input per piping</span><span class="sxs-lookup"><span data-stu-id="e02ab-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e02ab-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e02ab-118">-Name</span></span>
<span data-ttu-id="e02ab-119">Nome della capacità incorporata di PowerBI</span><span class="sxs-lookup"><span data-stu-id="e02ab-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02ab-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e02ab-120">-PassThru</span></span>
<span data-ttu-id="e02ab-121">Restituirà i dettagli della capacità eliminata se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="e02ab-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="e02ab-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e02ab-122">-ResourceGroupName</span></span>
<span data-ttu-id="e02ab-123">Nome del gruppo di risorse Azure a cui appartiene la capacità</span><span class="sxs-lookup"><span data-stu-id="e02ab-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02ab-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e02ab-124">-ResourceId</span></span>
<span data-ttu-id="e02ab-125">ID risorsa di Azure</span><span class="sxs-lookup"><span data-stu-id="e02ab-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02ab-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e02ab-126">-Confirm</span></span>
<span data-ttu-id="e02ab-127">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="e02ab-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="e02ab-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e02ab-128">-WhatIf</span></span>
<span data-ttu-id="e02ab-129">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="e02ab-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="e02ab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02ab-130">CommonParameters</span></span>
<span data-ttu-id="e02ab-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e02ab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02ab-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e02ab-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02ab-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e02ab-133">INPUTS</span></span>

### <span data-ttu-id="e02ab-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e02ab-134">System.String</span></span>

### <span data-ttu-id="e02ab-135">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e02ab-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="e02ab-136">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e02ab-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e02ab-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e02ab-137">OUTPUTS</span></span>

### <span data-ttu-id="e02ab-138">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e02ab-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="e02ab-139">Note</span><span class="sxs-lookup"><span data-stu-id="e02ab-139">NOTES</span></span>

## <span data-ttu-id="e02ab-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e02ab-140">RELATED LINKS</span></span>

[<span data-ttu-id="e02ab-141">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e02ab-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="e02ab-142">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="e02ab-142">New-AzureRmPowerBIEmbeddedCapacity</span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)
