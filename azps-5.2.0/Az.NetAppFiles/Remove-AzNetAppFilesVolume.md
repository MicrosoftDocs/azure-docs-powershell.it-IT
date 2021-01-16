---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: 9400efa61a98b6eb80b975d4999e03eb872e3b28
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361101"
---
# <span data-ttu-id="28c91-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="28c91-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="28c91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28c91-102">SYNOPSIS</span></span>
<span data-ttu-id="28c91-103">Elimina un volume di Azure NetApp file (ANF).</span><span class="sxs-lookup"><span data-stu-id="28c91-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="28c91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28c91-104">SYNTAX</span></span>

### <span data-ttu-id="28c91-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="28c91-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28c91-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28c91-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28c91-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28c91-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28c91-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28c91-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28c91-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28c91-109">DESCRIPTION</span></span>
<span data-ttu-id="28c91-110">Il cmdlet **Remove-AzNetAppFilesVolume** Elimina un volume di ANF.</span><span class="sxs-lookup"><span data-stu-id="28c91-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="28c91-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28c91-111">EXAMPLES</span></span>

### <span data-ttu-id="28c91-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28c91-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="28c91-113">Questo comando Elimina il volume ANF "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="28c91-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="28c91-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28c91-114">PARAMETERS</span></span>

### <span data-ttu-id="28c91-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="28c91-115">-AccountName</span></span>
<span data-ttu-id="28c91-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="28c91-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="28c91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c91-117">-DefaultProfile</span></span>
<span data-ttu-id="28c91-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28c91-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28c91-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28c91-119">-InputObject</span></span>
<span data-ttu-id="28c91-120">Oggetto volume da rimuovere</span><span class="sxs-lookup"><span data-stu-id="28c91-120">The volume object to remove</span></span>

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

### <span data-ttu-id="28c91-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="28c91-121">-Name</span></span>
<span data-ttu-id="28c91-122">Nome del volume di ANF</span><span class="sxs-lookup"><span data-stu-id="28c91-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="28c91-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28c91-123">-PassThru</span></span>
<span data-ttu-id="28c91-124">Restituirà se il volume specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="28c91-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="28c91-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="28c91-125">-PoolName</span></span>
<span data-ttu-id="28c91-126">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="28c91-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="28c91-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="28c91-127">-PoolObject</span></span>
<span data-ttu-id="28c91-128">Oggetto pool contenente il volume da rimuovere</span><span class="sxs-lookup"><span data-stu-id="28c91-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="28c91-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28c91-129">-ResourceGroupName</span></span>
<span data-ttu-id="28c91-130">Gruppo risorse del volume ANF</span><span class="sxs-lookup"><span data-stu-id="28c91-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="28c91-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28c91-131">-ResourceId</span></span>
<span data-ttu-id="28c91-132">ID risorsa del volume ANF</span><span class="sxs-lookup"><span data-stu-id="28c91-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="28c91-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="28c91-133">-Confirm</span></span>
<span data-ttu-id="28c91-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28c91-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28c91-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28c91-135">-WhatIf</span></span>
<span data-ttu-id="28c91-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28c91-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28c91-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28c91-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28c91-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c91-138">CommonParameters</span></span>
<span data-ttu-id="28c91-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28c91-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c91-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28c91-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c91-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28c91-141">INPUTS</span></span>

### <span data-ttu-id="28c91-142">System. String</span><span class="sxs-lookup"><span data-stu-id="28c91-142">System.String</span></span>

### <span data-ttu-id="28c91-143">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="28c91-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="28c91-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="28c91-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="28c91-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28c91-145">OUTPUTS</span></span>

### <span data-ttu-id="28c91-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28c91-146">System.Boolean</span></span>

## <span data-ttu-id="28c91-147">Note</span><span class="sxs-lookup"><span data-stu-id="28c91-147">NOTES</span></span>

## <span data-ttu-id="28c91-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28c91-148">RELATED LINKS</span></span>
