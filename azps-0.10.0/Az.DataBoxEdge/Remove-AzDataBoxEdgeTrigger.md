---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 363a6ea9cc6b53ca0c8a75fd32db5222e332bc98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861569"
---
# <span data-ttu-id="0db85-101">Remove-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="0db85-101">Remove-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="0db85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0db85-102">SYNOPSIS</span></span>
<span data-ttu-id="0db85-103">Rimuove un trigger esistente nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0db85-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="0db85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0db85-104">SYNTAX</span></span>

### <span data-ttu-id="0db85-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0db85-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0db85-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0db85-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0db85-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0db85-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-InputObject] <PSDataBoxEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0db85-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0db85-108">DESCRIPTION</span></span>
<span data-ttu-id="0db85-109">Il cmdlet **Remove-AzDataBoxEdgeTrigger** rimuove un trigger esistente nel dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="0db85-109">The **Remove-AzDataBoxEdgeTrigger** cmdlet removes an existing trigger on the Data Box Edge device.</span></span>

## <span data-ttu-id="0db85-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0db85-110">EXAMPLES</span></span>

### <span data-ttu-id="0db85-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0db85-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="0db85-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0db85-112">PARAMETERS</span></span>

### <span data-ttu-id="0db85-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0db85-113">-AsJob</span></span>
<span data-ttu-id="0db85-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0db85-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0db85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db85-115">-DefaultProfile</span></span>
<span data-ttu-id="0db85-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0db85-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0db85-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0db85-117">-DeviceName</span></span>
<span data-ttu-id="0db85-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="0db85-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db85-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0db85-119">-InputObject</span></span>
<span data-ttu-id="0db85-120">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="0db85-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0db85-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0db85-121">-Name</span></span>
<span data-ttu-id="0db85-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="0db85-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db85-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0db85-123">-PassThru</span></span>
<span data-ttu-id="0db85-124">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="0db85-124">returns true if successful</span></span>

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

### <span data-ttu-id="0db85-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db85-125">-ResourceGroupName</span></span>
<span data-ttu-id="0db85-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="0db85-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db85-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0db85-127">-ResourceId</span></span>
<span data-ttu-id="0db85-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0db85-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db85-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0db85-129">-Confirm</span></span>
<span data-ttu-id="0db85-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0db85-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0db85-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0db85-131">-WhatIf</span></span>
<span data-ttu-id="0db85-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0db85-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0db85-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0db85-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0db85-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db85-134">CommonParameters</span></span>
<span data-ttu-id="0db85-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db85-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db85-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0db85-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db85-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0db85-137">INPUTS</span></span>

### <span data-ttu-id="0db85-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0db85-138">System.String</span></span>

### <span data-ttu-id="0db85-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="0db85-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="0db85-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0db85-140">OUTPUTS</span></span>

### <span data-ttu-id="0db85-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0db85-141">System.Boolean</span></span>

## <span data-ttu-id="0db85-142">Note</span><span class="sxs-lookup"><span data-stu-id="0db85-142">NOTES</span></span>

## <span data-ttu-id="0db85-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0db85-143">RELATED LINKS</span></span>
