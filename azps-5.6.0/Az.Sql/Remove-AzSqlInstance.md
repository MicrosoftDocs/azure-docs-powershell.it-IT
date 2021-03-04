---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: a8985d77ba1bbf33e49f353ad39d287f7bd3979b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955150"
---
# <span data-ttu-id="71b93-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="71b93-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="71b93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71b93-102">SYNOPSIS</span></span>
<span data-ttu-id="71b93-103">Rimuove un'istanza SQL di database gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="71b93-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="71b93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71b93-104">SYNTAX</span></span>

### <span data-ttu-id="71b93-105">RemoveInstanceFromInputParameters (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71b93-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71b93-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="71b93-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71b93-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="71b93-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71b93-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="71b93-108">DESCRIPTION</span></span>
<span data-ttu-id="71b93-109">Il cmdlet **Remove-AzSqlInstance** rimuove un'istanza gestita SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="71b93-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="71b93-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71b93-110">EXAMPLES</span></span>

### <span data-ttu-id="71b93-111">Esempio 1: Rimuovere un'istanza</span><span class="sxs-lookup"><span data-stu-id="71b93-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="71b93-112">Questo comando rimuove l'istanza denominata managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="71b93-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="71b93-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71b93-113">PARAMETERS</span></span>

### <span data-ttu-id="71b93-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71b93-114">-DefaultProfile</span></span>
<span data-ttu-id="71b93-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71b93-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71b93-116">-Force</span><span class="sxs-lookup"><span data-stu-id="71b93-116">-Force</span></span>
<span data-ttu-id="71b93-117">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="71b93-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="71b93-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71b93-118">-InputObject</span></span>
<span data-ttu-id="71b93-119">Oggetto AzureSqlManagedInstanceModel da rimuovere</span><span class="sxs-lookup"><span data-stu-id="71b93-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71b93-120">-Name</span><span class="sxs-lookup"><span data-stu-id="71b93-120">-Name</span></span>
<span data-ttu-id="71b93-121">SQL di istanza.</span><span class="sxs-lookup"><span data-stu-id="71b93-121">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b93-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71b93-122">-ResourceGroupName</span></span>
<span data-ttu-id="71b93-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="71b93-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b93-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71b93-124">-ResourceId</span></span>
<span data-ttu-id="71b93-125">ID risorsa dell'oggetto istanza da rimuovere</span><span class="sxs-lookup"><span data-stu-id="71b93-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b93-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71b93-126">-Confirm</span></span>
<span data-ttu-id="71b93-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71b93-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71b93-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71b93-128">-WhatIf</span></span>
<span data-ttu-id="71b93-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71b93-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71b93-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71b93-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71b93-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b93-131">CommonParameters</span></span>
<span data-ttu-id="71b93-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71b93-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b93-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="71b93-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b93-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="71b93-134">INPUTS</span></span>

### <span data-ttu-id="71b93-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="71b93-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="71b93-136">System.String</span><span class="sxs-lookup"><span data-stu-id="71b93-136">System.String</span></span>

## <span data-ttu-id="71b93-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71b93-137">OUTPUTS</span></span>

### <span data-ttu-id="71b93-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="71b93-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="71b93-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="71b93-139">NOTES</span></span>

## <span data-ttu-id="71b93-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71b93-140">RELATED LINKS</span></span>
