---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
ms.openlocfilehash: c3fa71b6fb54f359f035f4f6c2f18789ff24b3ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192142"
---
# <span data-ttu-id="3f2a2-101">Invoke-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="3f2a2-101">Invoke-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="3f2a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f2a2-102">SYNOPSIS</span></span>
<span data-ttu-id="3f2a2-103">Richiama azioni specifiche su una condivisione.</span><span class="sxs-lookup"><span data-stu-id="3f2a2-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="3f2a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f2a2-104">SYNTAX</span></span>

### <span data-ttu-id="3f2a2-105">InvokeByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3f2a2-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f2a2-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f2a2-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f2a2-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f2a2-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f2a2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f2a2-108">DESCRIPTION</span></span>
<span data-ttu-id="3f2a2-109">Il cmdlet **Invoke-AzDataBoxEdgeShare** richiama l'azione per aggiornare i dati in una condivisione in un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="3f2a2-109">The **Invoke-AzDataBoxEdgeShare** cmdlet invokes action to refresh data on a share on a Data Box Edge device.</span></span>

## <span data-ttu-id="3f2a2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f2a2-110">EXAMPLES</span></span>

### <span data-ttu-id="3f2a2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3f2a2-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="3f2a2-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3f2a2-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzDataBoxEdgeShare
```

## <span data-ttu-id="3f2a2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f2a2-113">PARAMETERS</span></span>

### <span data-ttu-id="3f2a2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f2a2-114">-AsJob</span></span>
<span data-ttu-id="3f2a2-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3f2a2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f2a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f2a2-116">-DefaultProfile</span></span>
<span data-ttu-id="3f2a2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f2a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f2a2-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3f2a2-118">-DeviceName</span></span>
<span data-ttu-id="3f2a2-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="3f2a2-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f2a2-120">-InputObject</span></span>
<span data-ttu-id="3f2a2-121">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="3f2a2-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f2a2-122">-Name</span></span>
<span data-ttu-id="3f2a2-123">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="3f2a2-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f2a2-124">-PassThru</span></span>
<span data-ttu-id="3f2a2-125">Restituisce vero in caso di esito positivo</span><span class="sxs-lookup"><span data-stu-id="3f2a2-125">returns true if successful</span></span>

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

### <span data-ttu-id="3f2a2-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="3f2a2-126">-RefreshData</span></span>
<span data-ttu-id="3f2a2-127">Aggiornare i metadati di condivisione con i dati del cloud</span><span class="sxs-lookup"><span data-stu-id="3f2a2-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="3f2a2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f2a2-128">-ResourceGroupName</span></span>
<span data-ttu-id="3f2a2-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="3f2a2-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f2a2-130">-ResourceId</span></span>
<span data-ttu-id="3f2a2-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f2a2-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f2a2-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3f2a2-132">-Confirm</span></span>
<span data-ttu-id="3f2a2-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f2a2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f2a2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f2a2-134">-WhatIf</span></span>
<span data-ttu-id="3f2a2-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f2a2-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f2a2-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f2a2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f2a2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f2a2-137">CommonParameters</span></span>
<span data-ttu-id="3f2a2-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f2a2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f2a2-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f2a2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f2a2-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f2a2-140">INPUTS</span></span>

### <span data-ttu-id="3f2a2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3f2a2-141">System.String</span></span>

### <span data-ttu-id="3f2a2-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="3f2a2-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="3f2a2-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f2a2-143">OUTPUTS</span></span>

### <span data-ttu-id="3f2a2-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f2a2-144">System.Boolean</span></span>

## <span data-ttu-id="3f2a2-145">Note</span><span class="sxs-lookup"><span data-stu-id="3f2a2-145">NOTES</span></span>

## <span data-ttu-id="3f2a2-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f2a2-146">RELATED LINKS</span></span>
