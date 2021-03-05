---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/set-aznetAppfilesvolumepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
ms.openlocfilehash: 2b3cf6588f32fd958073ced8d3347733416037ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968174"
---
# <span data-ttu-id="48af1-101">Set-AzNetAppFilesVolumePool</span><span class="sxs-lookup"><span data-stu-id="48af1-101">Set-AzNetAppFilesVolumePool</span></span>

## <span data-ttu-id="48af1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48af1-102">SYNOPSIS</span></span>
<span data-ttu-id="48af1-103">Cambiare pool per un volume di file Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="48af1-103">Change pool for an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="48af1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48af1-104">SYNTAX</span></span>

### <span data-ttu-id="48af1-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48af1-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-NewPoolResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48af1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48af1-106">ByParentObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -Name <String> -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48af1-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48af1-107">ByResourceIdParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48af1-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48af1-108">ByObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48af1-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="48af1-109">DESCRIPTION</span></span>
<span data-ttu-id="48af1-110">Il cmdlet **Set-AzNetAppFilesVolumePool** modifica il pool di un volume ANF.</span><span class="sxs-lookup"><span data-stu-id="48af1-110">The **Set-AzNetAppFilesVolumePool** cmdlet changes the pool of an ANF volume.</span></span>

## <span data-ttu-id="48af1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48af1-111">EXAMPLES</span></span>

### <span data-ttu-id="48af1-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="48af1-112">Example 1</span></span>
```powershell
PS C:\>Set-AzNetAppFilesVolumePool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -NewPoolResourceId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="48af1-113">Il pool per il volume MyVolume viene modificato in uno con ID 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="48af1-113">This changes the pool for the volume MyVolume to one with the Id of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="48af1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48af1-114">PARAMETERS</span></span>

### <span data-ttu-id="48af1-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="48af1-115">-AccountName</span></span>
<span data-ttu-id="48af1-116">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="48af1-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48af1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48af1-117">-DefaultProfile</span></span>
<span data-ttu-id="48af1-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48af1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48af1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48af1-119">-InputObject</span></span>
<span data-ttu-id="48af1-120">L'oggetto volume da spostare</span><span class="sxs-lookup"><span data-stu-id="48af1-120">The volume object to move</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48af1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="48af1-121">-Name</span></span>
<span data-ttu-id="48af1-122">Nome del volume ANF</span><span class="sxs-lookup"><span data-stu-id="48af1-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48af1-123">-NewPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="48af1-123">-NewPoolResourceId</span></span>
<span data-ttu-id="48af1-124">ResourceId del pool di capacità in cui eseguire lo spostamento.</span><span class="sxs-lookup"><span data-stu-id="48af1-124">ResourceId of the capacity pool to move to.</span></span>
<span data-ttu-id="48af1-125">UUID v4 usato per identificare il pool</span><span class="sxs-lookup"><span data-stu-id="48af1-125">UUID v4 used to identify the pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48af1-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="48af1-126">-PoolName</span></span>
<span data-ttu-id="48af1-127">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="48af1-127">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48af1-128">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="48af1-128">-PoolObject</span></span>
<span data-ttu-id="48af1-129">Oggetto pool contenente il volume</span><span class="sxs-lookup"><span data-stu-id="48af1-129">The pool object containing the volume</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48af1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48af1-130">-ResourceGroupName</span></span>
<span data-ttu-id="48af1-131">Gruppo di risorse del volume ANF</span><span class="sxs-lookup"><span data-stu-id="48af1-131">The resource group of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48af1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48af1-132">-ResourceId</span></span>
<span data-ttu-id="48af1-133">ID risorsa del volume ANF</span><span class="sxs-lookup"><span data-stu-id="48af1-133">The resource id of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48af1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48af1-134">-Confirm</span></span>
<span data-ttu-id="48af1-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48af1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48af1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48af1-136">-WhatIf</span></span>
<span data-ttu-id="48af1-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48af1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48af1-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48af1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48af1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48af1-139">CommonParameters</span></span>
<span data-ttu-id="48af1-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48af1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48af1-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="48af1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48af1-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="48af1-142">INPUTS</span></span>

### <span data-ttu-id="48af1-143">System.String</span><span class="sxs-lookup"><span data-stu-id="48af1-143">System.String</span></span>

### <span data-ttu-id="48af1-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="48af1-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="48af1-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="48af1-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="48af1-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48af1-146">OUTPUTS</span></span>

### <span data-ttu-id="48af1-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="48af1-147">System.Boolean</span></span>

## <span data-ttu-id="48af1-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="48af1-148">NOTES</span></span>

## <span data-ttu-id="48af1-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48af1-149">RELATED LINKS</span></span>
