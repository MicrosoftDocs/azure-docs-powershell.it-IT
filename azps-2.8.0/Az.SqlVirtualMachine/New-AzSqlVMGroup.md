---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMGroup.md
ms.openlocfilehash: e46df689b4cc6953f29f5361c4df8bc5bd878acd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857642"
---
# <span data-ttu-id="fade4-101">New-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="fade4-101">New-AzSqlVMGroup</span></span>

## <span data-ttu-id="fade4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fade4-102">SYNOPSIS</span></span>
<span data-ttu-id="fade4-103">Crea un nuovo gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="fade4-103">Creates a new sql virtual machine group.</span></span>

## <span data-ttu-id="fade4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fade4-104">SYNTAX</span></span>

```
New-AzSqlVMGroup [-Location] <String> -Offer <String> -Sku <String> -ClusterOperatorAccount <String>
 -SqlServiceAccount <String> -StorageAccountUrl <String> -StorageAccountPrimaryKey <SecureString>
 -DomainFqdn <String> [-AsJob] [-OuPath <String>] [-FileShareWitnessPath <String>]
 [-ClusterBootstrapAccount <String>] [-Tag <Hashtable>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fade4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fade4-105">DESCRIPTION</span></span>
<span data-ttu-id="fade4-106">Il cmdlet New-AzSqlVMGroup crea un gruppo di macchine virtuali di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fade4-106">The New-AzSqlVMGroup cmdlet creates an Azure SQL virtual machine group.</span></span>

## <span data-ttu-id="fade4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fade4-107">EXAMPLES</span></span>

### <span data-ttu-id="fade4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fade4-108">Example 1</span></span>
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

<span data-ttu-id="fade4-109">Crea un nuovo gruppo di macchine virtuali di Azure SQL con il gruppo di test VM nel gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="fade4-109">Creates a new Azure SQL virtual machine group with test-group vm in the resource group ResourceGroup01.</span></span>
<span data-ttu-id="fade4-110">$profile è un oggetto di tipo Microsoft. Azure. Management. SqlVirtualMachine. Models. WsfcDomainProfile</span><span class="sxs-lookup"><span data-stu-id="fade4-110">$profile is an object of type Microsoft.Azure.Management.SqlVirtualMachine.Models.WsfcDomainProfile</span></span>

## <span data-ttu-id="fade4-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fade4-111">PARAMETERS</span></span>

### <span data-ttu-id="fade4-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fade4-112">-AsJob</span></span>
<span data-ttu-id="fade4-113">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="fade4-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="fade4-114">-ClusterBootstrapAccount</span><span class="sxs-lookup"><span data-stu-id="fade4-114">-ClusterBootstrapAccount</span></span>
<span data-ttu-id="fade4-115">Nome usato per la creazione di un cluster</span><span class="sxs-lookup"><span data-stu-id="fade4-115">Name used for creating cluster</span></span>

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

### <span data-ttu-id="fade4-116">-ClusterOperatorAccount</span><span class="sxs-lookup"><span data-stu-id="fade4-116">-ClusterOperatorAccount</span></span>
<span data-ttu-id="fade4-117">Nome usato per il cluster operativo</span><span class="sxs-lookup"><span data-stu-id="fade4-117">Name used for operating cluster</span></span>

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

### <span data-ttu-id="fade4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fade4-118">-DefaultProfile</span></span>
<span data-ttu-id="fade4-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fade4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fade4-120">-DomainFqdn</span><span class="sxs-lookup"><span data-stu-id="fade4-120">-DomainFqdn</span></span>
<span data-ttu-id="fade4-121">Nome completo del dominio</span><span class="sxs-lookup"><span data-stu-id="fade4-121">Fully qualified name of the domain</span></span>

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

### <span data-ttu-id="fade4-122">-FileShareWitnessPath</span><span class="sxs-lookup"><span data-stu-id="fade4-122">-FileShareWitnessPath</span></span>
<span data-ttu-id="fade4-123">Percorso facoltativo per il witness di condivisione file</span><span class="sxs-lookup"><span data-stu-id="fade4-123">Optional path for fileshare witness</span></span>

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

### <span data-ttu-id="fade4-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fade4-124">-Location</span></span>
<span data-ttu-id="fade4-125">Posizione del gruppo della macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="fade4-125">SQL virtual machine group location.</span></span>

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

### <span data-ttu-id="fade4-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="fade4-126">-Name</span></span>
<span data-ttu-id="fade4-127">Nome del gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="fade4-127">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="fade4-128">-Offerta</span><span class="sxs-lookup"><span data-stu-id="fade4-128">-Offer</span></span>
<span data-ttu-id="fade4-129">Offerta di un gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="fade4-129">SQL virtual machine group offer.</span></span>

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

### <span data-ttu-id="fade4-130">-OuPath</span><span class="sxs-lookup"><span data-stu-id="fade4-130">-OuPath</span></span>
<span data-ttu-id="fade4-131">Percorso unità organizzativa in cui saranno presenti i nodi e il cluster</span><span class="sxs-lookup"><span data-stu-id="fade4-131">Organizational Unit path in which the nodes and cluster will be present</span></span>

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

### <span data-ttu-id="fade4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fade4-132">-ResourceGroupName</span></span>
<span data-ttu-id="fade4-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fade4-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="fade4-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="fade4-134">-Sku</span></span>
<span data-ttu-id="fade4-135">Tipo di gruppo SQL Virtual Machine Edition.</span><span class="sxs-lookup"><span data-stu-id="fade4-135">SQL virtual machine group edition type.</span></span>

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

### <span data-ttu-id="fade4-136">-SqlServiceAccount</span><span class="sxs-lookup"><span data-stu-id="fade4-136">-SqlServiceAccount</span></span>
<span data-ttu-id="fade4-137">Nome in cui verrà eseguito il servizio SQL in tutte le macchine virtuali SQL partecipanti nel cluster</span><span class="sxs-lookup"><span data-stu-id="fade4-137">Name under which SQL service will run on all participating SQL virtual machines in the cluster</span></span>

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

### <span data-ttu-id="fade4-138">-StorageAccountPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="fade4-138">-StorageAccountPrimaryKey</span></span>
<span data-ttu-id="fade4-139">Chiave primaria dell'account di archiviazione dei testimoni</span><span class="sxs-lookup"><span data-stu-id="fade4-139">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="fade4-140">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="fade4-140">-StorageAccountUrl</span></span>
<span data-ttu-id="fade4-141">Chiave primaria dell'account di archiviazione dei testimoni</span><span class="sxs-lookup"><span data-stu-id="fade4-141">Primary key of the witness storage account</span></span>

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

### <span data-ttu-id="fade4-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="fade4-142">-Tag</span></span>
<span data-ttu-id="fade4-143">Tag da associare al gruppo SQL Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="fade4-143">The tags to associate with the SQL virtual machine group.</span></span>

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

### <span data-ttu-id="fade4-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fade4-144">-Confirm</span></span>
<span data-ttu-id="fade4-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fade4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fade4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fade4-146">-WhatIf</span></span>
<span data-ttu-id="fade4-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fade4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fade4-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fade4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fade4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fade4-149">CommonParameters</span></span>
<span data-ttu-id="fade4-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fade4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fade4-151">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fade4-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fade4-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fade4-152">INPUTS</span></span>

### <span data-ttu-id="fade4-153">System. String</span><span class="sxs-lookup"><span data-stu-id="fade4-153">System.String</span></span>

## <span data-ttu-id="fade4-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fade4-154">OUTPUTS</span></span>

### <span data-ttu-id="fade4-155">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="fade4-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="fade4-156">Note</span><span class="sxs-lookup"><span data-stu-id="fade4-156">NOTES</span></span>

## <span data-ttu-id="fade4-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fade4-157">RELATED LINKS</span></span>
