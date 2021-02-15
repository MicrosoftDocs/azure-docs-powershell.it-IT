---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzSqlVMGroup.md
ms.openlocfilehash: 885be17315e0dc0be8223f0d28bc11a6d6e41146
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195879"
---
# <span data-ttu-id="f4a3f-101">Update-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="f4a3f-101">Update-AzSqlVMGroup</span></span>

## <span data-ttu-id="f4a3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a3f-103">Aggiorna un gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="f4a3f-103">Updates a sql virtual machine group.</span></span>

## <span data-ttu-id="f4a3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4a3f-104">SYNTAX</span></span>

### <span data-ttu-id="f4a3f-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4a3f-105">Name (Default)</span></span>
```
Update-AzSqlVMGroup [-AsJob] [-ClusterOperatorAccount <String>] [-SqlServiceAccount <String>]
 [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>] [-DomainFqdn <String>]
 [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4a3f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f4a3f-106">InputObject</span></span>
```
Update-AzSqlVMGroup [-InputObject] <AzureSqlVMGroupModel> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4a3f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4a3f-107">ResourceId</span></span>
```
Update-AzSqlVMGroup [-ResourceId] <String> [-AsJob] [-ClusterOperatorAccount <String>]
 [-SqlServiceAccount <String>] [-StorageAccountUrl <String>] [-StorageAccountPrimaryKey <SecureString>]
 [-DomainFqdn <String>] [-OuPath <String>] [-FileShareWitnessPath <String>] [-ClusterBootstrapAccount <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4a3f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f4a3f-108">DESCRIPTION</span></span>
<span data-ttu-id="f4a3f-109">Il Update-AzSqlVMGroup cmdlet aggiorna un gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="f4a3f-109">The Update-AzSqlVMGroup cmdlet updates a sql virtual machine group.</span></span>

## <span data-ttu-id="f4a3f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4a3f-110">EXAMPLES</span></span>

### <span data-ttu-id="f4a3f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f4a3f-111">Example 1</span></span>
```powershell
PS C:\> $tags = @{'key'='value'}
PS C:\> $group = Update-AzSqlVMGroup -InputObject $group -Tags $tags
PS C:\> $group.Tags
Name                           Value
----                           -----
key                            value
```

<span data-ttu-id="f4a3f-112">Aggiorna i tag di un gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="f4a3f-112">Updates the tags of a sql virtual machine group.</span></span>

## <span data-ttu-id="f4a3f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4a3f-113">PARAMETERS</span></span>

### <span data-ttu-id="f4a3f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4a3f-114">-AsJob</span></span>
<span data-ttu-id="f4a3f-115">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="f4a3f-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f4a3f-116">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="f4a3f-116">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="f4a3f-117">Nome usato per la creazione del cluster</span><span class="sxs-lookup"><span data-stu-id="f4a3f-117">Name used for creating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a3f-118">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="f4a3f-118">-ClusterOperatorAccount</span></span>
<span data-ttu-id="f4a3f-119">Nome usato per il cluster operativo</span><span class="sxs-lookup"><span data-stu-id="f4a3f-119">Name used for operating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a3f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a3f-120">-DefaultProfile</span></span>
<span data-ttu-id="f4a3f-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4a3f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4a3f-122">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="f4a3f-122">-DomainFqdn</span></span>
<span data-ttu-id="f4a3f-123">Nome completo del dominio</span><span class="sxs-lookup"><span data-stu-id="f4a3f-123">Fully qualified name of the domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a3f-124">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="f4a3f-124">-FileShareWitnessPath</span></span>
<span data-ttu-id="f4a3f-125">Percorso facoltativo per condivisione file</span><span class="sxs-lookup"><span data-stu-id="f4a3f-125">Optional path for fileshare witness</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a3f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4a3f-126">-InputObject</span></span>
<span data-ttu-id="f4a3f-127">SQL dell'oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f4a3f-127">SQL virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: InputObject
Aliases: SqlVMGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4a3f-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f4a3f-128">-Name</span></span>
<span data-ttu-id="f4a3f-129">SQL del gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="f4a3f-129">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a3f-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="f4a3f-130">-OuPath</span></span>
<span data-ttu-id="f4a3f-131">Percorso dell'unità organizzativa in cui saranno presenti i nodi e il cluster</span><span class="sxs-lookup"><span data-stu-id="f4a3f-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a3f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4a3f-132">-ResourceGroupName</span></span>
<span data-ttu-id="f4a3f-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f4a3f-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a3f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4a3f-134">-ResourceId</span></span>
<span data-ttu-id="f4a3f-135">SQL ID risorsa gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="f4a3f-135">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4a3f-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="f4a3f-136">-SqlServiceAccount</span></span>
<span data-ttu-id="f4a3f-137">Nome in base al quale SQL verrà eseguito in tutte le macchine SQL partecipanti nel cluster</span><span class="sxs-lookup"><span data-stu-id="f4a3f-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a3f-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="f4a3f-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="f4a3f-139">Chiave primaria dell'account di archiviazione personale</span><span class="sxs-lookup"><span data-stu-id="f4a3f-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a3f-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="f4a3f-140">-StorageAccountUrl</span></span>
<span data-ttu-id="f4a3f-141">Chiave primaria dell'account di archiviazione personale</span><span class="sxs-lookup"><span data-stu-id="f4a3f-141">Primary key of the witness storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a3f-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4a3f-142">-Tag</span></span>
<span data-ttu-id="f4a3f-143">I tag da associare al gruppo SQL di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="f4a3f-143">The tags to associate with the SQL virtual machine group.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a3f-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4a3f-144">-Confirm</span></span>
<span data-ttu-id="f4a3f-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4a3f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4a3f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4a3f-146">-WhatIf</span></span>
<span data-ttu-id="f4a3f-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4a3f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4a3f-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4a3f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4a3f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a3f-149">CommonParameters</span></span>
<span data-ttu-id="f4a3f-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4a3f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a3f-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f4a3f-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a3f-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="f4a3f-152">INPUTS</span></span>

### <span data-ttu-id="f4a3f-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="f4a3f-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

### <span data-ttu-id="f4a3f-154">System.String</span><span class="sxs-lookup"><span data-stu-id="f4a3f-154">System.String</span></span>

## <span data-ttu-id="f4a3f-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4a3f-155">OUTPUTS</span></span>

### <span data-ttu-id="f4a3f-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="f4a3f-156">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="f4a3f-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="f4a3f-157">NOTES</span></span>

## <span data-ttu-id="f4a3f-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4a3f-158">RELATED LINKS</span></span>
