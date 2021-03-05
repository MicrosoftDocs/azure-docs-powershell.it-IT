---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: de9d0cf5d989cfa4d910f8e5ee9d959393c42632
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968333"
---
# <span data-ttu-id="b486a-101">Remove-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b486a-101">Remove-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="b486a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b486a-102">SYNOPSIS</span></span>
<span data-ttu-id="b486a-103">Elimina un criterio di backup dei file ANF di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="b486a-103">Deletes an Azure NetApp Files (ANF) backup policy.</span></span>

## <span data-ttu-id="b486a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b486a-104">SYNTAX</span></span>

### <span data-ttu-id="b486a-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b486a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b486a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b486a-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b486a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b486a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b486a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b486a-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -InputObject <PSNetAppFilesBackupPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b486a-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b486a-109">DESCRIPTION</span></span>
<span data-ttu-id="b486a-110">Il cmdlet **Remove-AzNetAppFilesBackupPolicy** elimina un criterio di backup ANF.</span><span class="sxs-lookup"><span data-stu-id="b486a-110">The **Remove-AzNetAppFilesBackupPolicy** cmdlet deletes an ANF backup policy.</span></span>

## <span data-ttu-id="b486a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b486a-111">EXAMPLES</span></span>

### <span data-ttu-id="b486a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b486a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="b486a-113">Questo comando elimina il nuovo criterio di backup ANF con il nome "MyBackupPolicy" per l'account "MyAccount".</span><span class="sxs-lookup"><span data-stu-id="b486a-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="b486a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b486a-114">PARAMETERS</span></span>

### <span data-ttu-id="b486a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b486a-115">-AccountName</span></span>
<span data-ttu-id="b486a-116">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="b486a-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="b486a-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="b486a-117">-AccountObject</span></span>
<span data-ttu-id="b486a-118">Oggetto Account che contiene i criteri di backup da rimuovere</span><span class="sxs-lookup"><span data-stu-id="b486a-118">The Account object containing the Backup Policy to remove</span></span>

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

### <span data-ttu-id="b486a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b486a-119">-DefaultProfile</span></span>
<span data-ttu-id="b486a-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b486a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b486a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b486a-121">-InputObject</span></span>
<span data-ttu-id="b486a-122">Oggetto BackupPolicy da rimuovere</span><span class="sxs-lookup"><span data-stu-id="b486a-122">The BackupPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b486a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b486a-123">-Name</span></span>
<span data-ttu-id="b486a-124">Nome dei criteri di backup ANF</span><span class="sxs-lookup"><span data-stu-id="b486a-124">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b486a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b486a-125">-PassThru</span></span>
<span data-ttu-id="b486a-126">Verificare se il criterio di backup specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="b486a-126">Return whether the specified backup policy was successfully removed</span></span>

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

### <span data-ttu-id="b486a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b486a-127">-ResourceGroupName</span></span>
<span data-ttu-id="b486a-128">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="b486a-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b486a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b486a-129">-ResourceId</span></span>
<span data-ttu-id="b486a-130">ID risorsa dei criteri di backup ANF</span><span class="sxs-lookup"><span data-stu-id="b486a-130">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="b486a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b486a-131">-Confirm</span></span>
<span data-ttu-id="b486a-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b486a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b486a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b486a-133">-WhatIf</span></span>
<span data-ttu-id="b486a-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b486a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b486a-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b486a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b486a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b486a-136">CommonParameters</span></span>
<span data-ttu-id="b486a-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b486a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b486a-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b486a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b486a-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="b486a-139">INPUTS</span></span>

### <span data-ttu-id="b486a-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b486a-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="b486a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b486a-141">System.String</span></span>

### <span data-ttu-id="b486a-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b486a-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="b486a-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b486a-143">OUTPUTS</span></span>

### <span data-ttu-id="b486a-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b486a-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="b486a-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="b486a-145">NOTES</span></span>

## <span data-ttu-id="b486a-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b486a-146">RELATED LINKS</span></span>
