---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: 9400efa61a98b6eb80b975d4999e03eb872e3b28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187270"
---
# <span data-ttu-id="f4290-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f4290-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="f4290-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4290-102">SYNOPSIS</span></span>
<span data-ttu-id="f4290-103">Elimina un volume di file ANF (Azure NetApp).</span><span class="sxs-lookup"><span data-stu-id="f4290-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="f4290-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4290-104">SYNTAX</span></span>

### <span data-ttu-id="f4290-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4290-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4290-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4290-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4290-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4290-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4290-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4290-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4290-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f4290-109">DESCRIPTION</span></span>
<span data-ttu-id="f4290-110">Il cmdlet **Remove-AzNetAppFilesVolume** elimina un volume ANF.</span><span class="sxs-lookup"><span data-stu-id="f4290-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="f4290-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4290-111">EXAMPLES</span></span>

### <span data-ttu-id="f4290-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f4290-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="f4290-113">Questo comando elimina il volume ANF "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="f4290-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="f4290-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4290-114">PARAMETERS</span></span>

### <span data-ttu-id="f4290-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f4290-115">-AccountName</span></span>
<span data-ttu-id="f4290-116">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="f4290-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="f4290-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4290-117">-DefaultProfile</span></span>
<span data-ttu-id="f4290-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4290-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4290-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4290-119">-InputObject</span></span>
<span data-ttu-id="f4290-120">L'oggetto volume da rimuovere</span><span class="sxs-lookup"><span data-stu-id="f4290-120">The volume object to remove</span></span>

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

### <span data-ttu-id="f4290-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f4290-121">-Name</span></span>
<span data-ttu-id="f4290-122">Nome del volume ANF</span><span class="sxs-lookup"><span data-stu-id="f4290-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="f4290-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4290-123">-PassThru</span></span>
<span data-ttu-id="f4290-124">Verificare se il volume specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="f4290-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="f4290-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f4290-125">-PoolName</span></span>
<span data-ttu-id="f4290-126">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="f4290-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="f4290-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="f4290-127">-PoolObject</span></span>
<span data-ttu-id="f4290-128">Oggetto pool contenente il volume da rimuovere</span><span class="sxs-lookup"><span data-stu-id="f4290-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="f4290-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4290-129">-ResourceGroupName</span></span>
<span data-ttu-id="f4290-130">Gruppo di risorse del volume ANF</span><span class="sxs-lookup"><span data-stu-id="f4290-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="f4290-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4290-131">-ResourceId</span></span>
<span data-ttu-id="f4290-132">ID risorsa del volume ANF</span><span class="sxs-lookup"><span data-stu-id="f4290-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="f4290-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4290-133">-Confirm</span></span>
<span data-ttu-id="f4290-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4290-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4290-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4290-135">-WhatIf</span></span>
<span data-ttu-id="f4290-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4290-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4290-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4290-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4290-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4290-138">CommonParameters</span></span>
<span data-ttu-id="f4290-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4290-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4290-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f4290-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4290-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="f4290-141">INPUTS</span></span>

### <span data-ttu-id="f4290-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f4290-142">System.String</span></span>

### <span data-ttu-id="f4290-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f4290-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="f4290-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f4290-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f4290-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4290-145">OUTPUTS</span></span>

### <span data-ttu-id="f4290-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f4290-146">System.Boolean</span></span>

## <span data-ttu-id="f4290-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="f4290-147">NOTES</span></span>

## <span data-ttu-id="f4290-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4290-148">RELATED LINKS</span></span>
