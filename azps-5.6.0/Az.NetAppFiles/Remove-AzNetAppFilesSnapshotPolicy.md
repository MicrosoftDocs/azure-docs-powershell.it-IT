---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 06bdb5246cc0830ef78baa81d418f1fe6e51e935
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968286"
---
# <span data-ttu-id="ac5d9-101">Remove-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="ac5d9-101">Remove-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="ac5d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac5d9-102">SYNOPSIS</span></span>
<span data-ttu-id="ac5d9-103">Elimina i criteri snapshot dei file (ANF) di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="ac5d9-103">Deletes an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="ac5d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac5d9-104">SYNTAX</span></span>

### <span data-ttu-id="ac5d9-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ac5d9-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac5d9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac5d9-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac5d9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac5d9-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac5d9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac5d9-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -InputObject <PSNetAppFilesSnapshotPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac5d9-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ac5d9-109">DESCRIPTION</span></span>
<span data-ttu-id="ac5d9-110">Il cmdlet **Remove-AzNetAppFilesSnapshotPolicy** elimina un criterio snapshot ANF.</span><span class="sxs-lookup"><span data-stu-id="ac5d9-110">The **Remove-AzNetAppFilesSnapshotPolicy** cmdlet deletes an ANF snapshot policy.</span></span>

## <span data-ttu-id="ac5d9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac5d9-111">EXAMPLES</span></span>

### <span data-ttu-id="ac5d9-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ac5d9-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="ac5d9-113">Questo comando elimina il nuovo criterio di backup ANF con il nome "MyBackupPolicy" per l'account "MyAccount".</span><span class="sxs-lookup"><span data-stu-id="ac5d9-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="ac5d9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac5d9-114">PARAMETERS</span></span>

### <span data-ttu-id="ac5d9-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ac5d9-115">-AccountName</span></span>
<span data-ttu-id="ac5d9-116">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="ac5d9-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="ac5d9-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="ac5d9-117">-AccountObject</span></span>
<span data-ttu-id="ac5d9-118">Account per il nuovo oggetto Criterio snapshot</span><span class="sxs-lookup"><span data-stu-id="ac5d9-118">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac5d9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac5d9-119">-DefaultProfile</span></span>
<span data-ttu-id="ac5d9-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac5d9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac5d9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac5d9-121">-InputObject</span></span>
<span data-ttu-id="ac5d9-122">Oggetto SnapshotPolicy da rimuovere</span><span class="sxs-lookup"><span data-stu-id="ac5d9-122">The SnapshotPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac5d9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ac5d9-123">-Name</span></span>
<span data-ttu-id="ac5d9-124">Nome dei criteri snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="ac5d9-124">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac5d9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac5d9-125">-PassThru</span></span>
<span data-ttu-id="ac5d9-126">Restituire se l'account specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="ac5d9-126">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="ac5d9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac5d9-127">-ResourceGroupName</span></span>
<span data-ttu-id="ac5d9-128">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="ac5d9-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="ac5d9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac5d9-129">-ResourceId</span></span>
<span data-ttu-id="ac5d9-130">ID risorsa dei criteri snapshot ANF</span><span class="sxs-lookup"><span data-stu-id="ac5d9-130">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="ac5d9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac5d9-131">-Confirm</span></span>
<span data-ttu-id="ac5d9-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac5d9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac5d9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac5d9-133">-WhatIf</span></span>
<span data-ttu-id="ac5d9-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac5d9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac5d9-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac5d9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac5d9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac5d9-136">CommonParameters</span></span>
<span data-ttu-id="ac5d9-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac5d9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac5d9-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ac5d9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac5d9-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="ac5d9-139">INPUTS</span></span>

### <span data-ttu-id="ac5d9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ac5d9-140">System.String</span></span>

### <span data-ttu-id="ac5d9-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ac5d9-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="ac5d9-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="ac5d9-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="ac5d9-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac5d9-143">OUTPUTS</span></span>

### <span data-ttu-id="ac5d9-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="ac5d9-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="ac5d9-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="ac5d9-145">NOTES</span></span>

## <span data-ttu-id="ac5d9-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac5d9-146">RELATED LINKS</span></span>
