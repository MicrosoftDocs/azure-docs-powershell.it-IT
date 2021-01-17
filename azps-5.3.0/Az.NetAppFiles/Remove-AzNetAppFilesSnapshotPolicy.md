---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 6ea65189969e38359bb6d4345ea4c47963f9eddf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380603"
---
# <span data-ttu-id="28577-101">Remove-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="28577-101">Remove-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="28577-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28577-102">SYNOPSIS</span></span>
<span data-ttu-id="28577-103">Elimina i criteri di snapshot di Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="28577-103">Deletes an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="28577-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28577-104">SYNTAX</span></span>

### <span data-ttu-id="28577-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="28577-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28577-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28577-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28577-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28577-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28577-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28577-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -InputObject <PSNetAppFilesSnapshotPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28577-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28577-109">DESCRIPTION</span></span>
<span data-ttu-id="28577-110">Il cmdlet **Remove-AzNetAppFilesSnapshotPolicy** Elimina i criteri di snapshot di ANF.</span><span class="sxs-lookup"><span data-stu-id="28577-110">The **Remove-AzNetAppFilesSnapshotPolicy** cmdlet deletes an ANF snapshot policy.</span></span>

## <span data-ttu-id="28577-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28577-111">EXAMPLES</span></span>

### <span data-ttu-id="28577-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28577-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="28577-113">Questo comando Elimina i nuovi criteri di backup di ANF con il nome "MyBackupPolicy" per l'account "conto".</span><span class="sxs-lookup"><span data-stu-id="28577-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="28577-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28577-114">PARAMETERS</span></span>

### <span data-ttu-id="28577-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="28577-115">-AccountName</span></span>
<span data-ttu-id="28577-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="28577-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="28577-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="28577-117">-AccountObject</span></span>
<span data-ttu-id="28577-118">Account per il nuovo oggetto Criteri snapshot</span><span class="sxs-lookup"><span data-stu-id="28577-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="28577-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28577-119">-DefaultProfile</span></span>
<span data-ttu-id="28577-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28577-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28577-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28577-121">-InputObject</span></span>
<span data-ttu-id="28577-122">Oggetto SnapshotPolicy da rimuovere</span><span class="sxs-lookup"><span data-stu-id="28577-122">The SnapshotPolicy object to remove</span></span>

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

### <span data-ttu-id="28577-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="28577-123">-Name</span></span>
<span data-ttu-id="28577-124">Nome dei criteri di snapshot di ANF</span><span class="sxs-lookup"><span data-stu-id="28577-124">The name of the ANF snapshot policy</span></span>

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

### <span data-ttu-id="28577-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28577-125">-PassThru</span></span>
<span data-ttu-id="28577-126">Restituisce se l'account specificato è stato rimosso correttamente</span><span class="sxs-lookup"><span data-stu-id="28577-126">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="28577-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28577-127">-ResourceGroupName</span></span>
<span data-ttu-id="28577-128">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="28577-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="28577-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28577-129">-ResourceId</span></span>
<span data-ttu-id="28577-130">ID risorsa dei criteri di snapshot di ANF</span><span class="sxs-lookup"><span data-stu-id="28577-130">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="28577-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="28577-131">-Confirm</span></span>
<span data-ttu-id="28577-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28577-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28577-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28577-133">-WhatIf</span></span>
<span data-ttu-id="28577-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28577-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28577-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28577-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28577-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28577-136">CommonParameters</span></span>
<span data-ttu-id="28577-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28577-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28577-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28577-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28577-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28577-139">INPUTS</span></span>

### <span data-ttu-id="28577-140">System. String</span><span class="sxs-lookup"><span data-stu-id="28577-140">System.String</span></span>

### <span data-ttu-id="28577-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="28577-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="28577-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="28577-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="28577-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28577-143">OUTPUTS</span></span>

### <span data-ttu-id="28577-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="28577-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="28577-145">Note</span><span class="sxs-lookup"><span data-stu-id="28577-145">NOTES</span></span>

## <span data-ttu-id="28577-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28577-146">RELATED LINKS</span></span>
