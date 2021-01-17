---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: ef0ad91d0294f0ac1a4a466a79ce436a7719af5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322652"
---
# <span data-ttu-id="03a52-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="03a52-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="03a52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03a52-102">SYNOPSIS</span></span>
<span data-ttu-id="03a52-103">Rimuove un cluster virtuale SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="03a52-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="03a52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03a52-104">SYNTAX</span></span>

### <span data-ttu-id="03a52-105">RemoveVirtualClusterFromInputParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="03a52-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03a52-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="03a52-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03a52-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="03a52-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03a52-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03a52-108">DESCRIPTION</span></span>
<span data-ttu-id="03a52-109">Il cmdlet **Remove-AzSqlVirtualCluster** rimuove un cluster virtuale di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="03a52-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="03a52-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03a52-110">EXAMPLES</span></span>

### <span data-ttu-id="03a52-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="03a52-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="03a52-112">Questo comando rimuove il cluster virtuale denominato VirtualCluster1 assegnato al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="03a52-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="03a52-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03a52-113">PARAMETERS</span></span>

### <span data-ttu-id="03a52-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03a52-114">-AsJob</span></span>
<span data-ttu-id="03a52-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="03a52-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03a52-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a52-116">-DefaultProfile</span></span>
<span data-ttu-id="03a52-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03a52-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03a52-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03a52-118">-InputObject</span></span>
<span data-ttu-id="03a52-119">Oggetto Instance da rimuovere</span><span class="sxs-lookup"><span data-stu-id="03a52-119">The instance object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel
Parameter Sets: RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition
Aliases: VirtualCluster

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03a52-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="03a52-120">-Name</span></span>
<span data-ttu-id="03a52-121">Nome del cluster virtuale.</span><span class="sxs-lookup"><span data-stu-id="03a52-121">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a52-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03a52-122">-ResourceGroupName</span></span>
<span data-ttu-id="03a52-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="03a52-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a52-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03a52-124">-ResourceId</span></span>
<span data-ttu-id="03a52-125">ID risorsa dell'oggetto Instance da rimuovere</span><span class="sxs-lookup"><span data-stu-id="03a52-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a52-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="03a52-126">-Confirm</span></span>
<span data-ttu-id="03a52-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03a52-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03a52-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03a52-128">-WhatIf</span></span>
<span data-ttu-id="03a52-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03a52-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03a52-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03a52-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03a52-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a52-131">CommonParameters</span></span>
<span data-ttu-id="03a52-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03a52-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a52-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03a52-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a52-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03a52-134">INPUTS</span></span>

### <span data-ttu-id="03a52-135">Microsoft. Azure. Commands. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="03a52-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="03a52-136">System. String</span><span class="sxs-lookup"><span data-stu-id="03a52-136">System.String</span></span>

## <span data-ttu-id="03a52-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03a52-137">OUTPUTS</span></span>

### <span data-ttu-id="03a52-138">Microsoft. Azure. Commands. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="03a52-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="03a52-139">Note</span><span class="sxs-lookup"><span data-stu-id="03a52-139">NOTES</span></span>

## <span data-ttu-id="03a52-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03a52-140">RELATED LINKS</span></span>
