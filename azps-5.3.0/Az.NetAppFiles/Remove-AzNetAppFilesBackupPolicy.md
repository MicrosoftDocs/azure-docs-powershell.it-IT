---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 975e451854a935034dc4ed508770f48e126807e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475549"
---
# <span data-ttu-id="4db8d-101">Remove-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="4db8d-101">Remove-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="4db8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4db8d-102">SYNOPSIS</span></span>
<span data-ttu-id="4db8d-103">Elimina i criteri di backup di Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="4db8d-103">Deletes an Azure NetApp Files (ANF) backup policy.</span></span>

## <span data-ttu-id="4db8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4db8d-104">SYNTAX</span></span>

### <span data-ttu-id="4db8d-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4db8d-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4db8d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4db8d-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4db8d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4db8d-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4db8d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4db8d-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -InputObject <PSNetAppFilesBackupPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4db8d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4db8d-109">DESCRIPTION</span></span>
<span data-ttu-id="4db8d-110">Il cmdlet **Remove-AzNetAppFilesBackupPolicy** Elimina i criteri di backup di ANF.</span><span class="sxs-lookup"><span data-stu-id="4db8d-110">The **Remove-AzNetAppFilesBackupPolicy** cmdlet deletes an ANF backup policy.</span></span>

## <span data-ttu-id="4db8d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4db8d-111">EXAMPLES</span></span>

### <span data-ttu-id="4db8d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4db8d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="4db8d-113">Questo comando Elimina i nuovi criteri di backup di ANF con il nome "MyBackupPolicy" per l'account "conto".</span><span class="sxs-lookup"><span data-stu-id="4db8d-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="4db8d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4db8d-114">PARAMETERS</span></span>

### <span data-ttu-id="4db8d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4db8d-115">-AccountName</span></span>
<span data-ttu-id="4db8d-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="4db8d-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="4db8d-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="4db8d-117">-AccountObject</span></span>
<span data-ttu-id="4db8d-118">Oggetto account che contiene i criteri di backup da rimuovere</span><span class="sxs-lookup"><span data-stu-id="4db8d-118">The Account object containing the Backup Policy to remove</span></span>

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

### <span data-ttu-id="4db8d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4db8d-119">-DefaultProfile</span></span>
<span data-ttu-id="4db8d-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4db8d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4db8d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4db8d-121">-InputObject</span></span>
<span data-ttu-id="4db8d-122">Oggetto BackupPolicy da rimuovere</span><span class="sxs-lookup"><span data-stu-id="4db8d-122">The BackupPolicy object to remove</span></span>

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

### <span data-ttu-id="4db8d-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="4db8d-123">-Name</span></span>
<span data-ttu-id="4db8d-124">Nome del criterio di backup di ANF</span><span class="sxs-lookup"><span data-stu-id="4db8d-124">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="4db8d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4db8d-125">-PassThru</span></span>
<span data-ttu-id="4db8d-126">Restituire se il criterio di backup specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="4db8d-126">Return whether the specified backup policy was successfully removed</span></span>

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

### <span data-ttu-id="4db8d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4db8d-127">-ResourceGroupName</span></span>
<span data-ttu-id="4db8d-128">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="4db8d-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="4db8d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4db8d-129">-ResourceId</span></span>
<span data-ttu-id="4db8d-130">ID risorsa dei criteri di backup di ANF</span><span class="sxs-lookup"><span data-stu-id="4db8d-130">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="4db8d-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4db8d-131">-Confirm</span></span>
<span data-ttu-id="4db8d-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4db8d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4db8d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4db8d-133">-WhatIf</span></span>
<span data-ttu-id="4db8d-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4db8d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4db8d-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4db8d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4db8d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db8d-136">CommonParameters</span></span>
<span data-ttu-id="4db8d-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4db8d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4db8d-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4db8d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db8d-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4db8d-139">INPUTS</span></span>

### <span data-ttu-id="4db8d-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="4db8d-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="4db8d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4db8d-141">System.String</span></span>

### <span data-ttu-id="4db8d-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="4db8d-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="4db8d-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4db8d-143">OUTPUTS</span></span>

### <span data-ttu-id="4db8d-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="4db8d-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="4db8d-145">Note</span><span class="sxs-lookup"><span data-stu-id="4db8d-145">NOTES</span></span>

## <span data-ttu-id="4db8d-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4db8d-146">RELATED LINKS</span></span>
