---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: bc9c881a69ee2365dcb9ff805c1c14fe3f1bbf79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978062"
---
# <span data-ttu-id="b0180-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="b0180-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="b0180-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0180-102">SYNOPSIS</span></span>
<span data-ttu-id="b0180-103">Crea un nuovo gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="b0180-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="b0180-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0180-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0180-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b0180-105">DESCRIPTION</span></span>
<span data-ttu-id="b0180-106">Il cmdlet New-AzSqlVMGroup crea un gruppo di SQL di macchine virtuali azure.</span><span class="sxs-lookup"><span data-stu-id="b0180-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="b0180-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0180-107">EXAMPLES</span></span>

### <span data-ttu-id="b0180-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b0180-108">Example 1</span></span>
```powershell
PS C:\> $secureKey = ConvertTo-SecureString $profile.StorageAccountPrimaryKey -AsPlainText -Force
PS C:\> New-AzSqlVMGroup $resourceGroupName $groupName $location -ClusterOperatorAccount $profile.ClusterOperatorAccount `
>>         -SqlServiceAccount $profile.SqlServiceAccount -StorageAccountUrl $profile.StorageAccountUrl `
>>         -StorageAccountPrimaryKey $secureKey -DomainFqdn $profile.DomainFqdn `
>>         -Offer 'SQL2017-WS2016' -Sku 'Developer'
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="b0180-109">Crea un nuovo gruppo di SQL virtuali Azure con macchina virtuale di gruppo di test nel gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="b0180-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="b0180-110">$profile è un oggetto di tipo Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span><span class="sxs-lookup"><span data-stu-id="b0180-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="b0180-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0180-111">PARAMETERS</span></span>

### <span data-ttu-id="b0180-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0180-112">-AsJob</span></span>
<span data-ttu-id="b0180-113">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="b0180-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b0180-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="b0180-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="b0180-115">Nome usato per la creazione del cluster</span><span class="sxs-lookup"><span data-stu-id="b0180-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="b0180-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="b0180-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="b0180-117">Nome usato per il cluster operativo</span><span class="sxs-lookup"><span data-stu-id="b0180-117">Name used for operating cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0180-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0180-118">-DefaultProfile</span></span>
<span data-ttu-id="b0180-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0180-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0180-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="b0180-120">-DomainFqdn</span></span>
<span data-ttu-id="b0180-121">Nome completo del dominio</span><span class="sxs-lookup"><span data-stu-id="b0180-121">Fully qualified name of the domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0180-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="b0180-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="b0180-123">Percorso facoltativo per condivisione file</span><span class="sxs-lookup"><span data-stu-id="b0180-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="b0180-124">-Location</span><span class="sxs-lookup"><span data-stu-id="b0180-124">-Location</span></span>
<span data-ttu-id="b0180-125">SQL del gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b0180-125">SQL virtual machine group location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0180-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b0180-126">-Name</span></span>
<span data-ttu-id="b0180-127">SQL del gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b0180-127">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0180-128">-Offerta</span><span class="sxs-lookup"><span data-stu-id="b0180-128">-Offer</span></span>
<span data-ttu-id="b0180-129">SQL di gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b0180-129">SQL virtual machine group offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0180-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="b0180-130">-OuPath</span></span>
<span data-ttu-id="b0180-131">Percorso dell'unità organizzativa in cui saranno presenti i nodi e il cluster</span><span class="sxs-lookup"><span data-stu-id="b0180-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="b0180-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0180-132">-ResourceGroupName</span></span>
<span data-ttu-id="b0180-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b0180-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0180-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="b0180-134">-Sku</span></span>
<span data-ttu-id="b0180-135">SQL di edizione di gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b0180-135">SQL virtual machine group edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0180-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="b0180-136">-SqlServiceAccount</span></span>
<span data-ttu-id="b0180-137">Nome in base al quale SQL verrà eseguito in tutte le macchine SQL partecipanti nel cluster</span><span class="sxs-lookup"><span data-stu-id="b0180-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0180-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b0180-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="b0180-139">Chiave primaria dell'account di archiviazione personale</span><span class="sxs-lookup"><span data-stu-id="b0180-139">Primary key of the witness storage account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0180-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="b0180-140">-StorageAccountUrl</span></span>
<span data-ttu-id="b0180-141">Chiave primaria dell'account di archiviazione personale</span><span class="sxs-lookup"><span data-stu-id="b0180-141">Primary key of the witness storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0180-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="b0180-142">-Tag</span></span>
<span data-ttu-id="b0180-143">I tag da associare al gruppo SQL di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b0180-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="b0180-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0180-144">-Confirm</span></span>
<span data-ttu-id="b0180-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0180-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0180-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0180-146">-WhatIf</span></span>
<span data-ttu-id="b0180-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0180-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0180-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0180-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0180-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0180-149">CommonParameters</span></span>
<span data-ttu-id="b0180-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0180-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0180-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b0180-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0180-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="b0180-152">INPUTS</span></span>

### <span data-ttu-id="b0180-153">System.String</span><span class="sxs-lookup"><span data-stu-id="b0180-153">System.String</span></span>

## <span data-ttu-id="b0180-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0180-154">OUTPUTS</span></span>

### <span data-ttu-id="b0180-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="b0180-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="b0180-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="b0180-156">NOTES</span></span>

## <span data-ttu-id="b0180-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0180-157">RELATED LINKS</span></span>
