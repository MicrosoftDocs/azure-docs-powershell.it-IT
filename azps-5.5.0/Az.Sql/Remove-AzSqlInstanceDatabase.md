---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabase.md
ms.openlocfilehash: a496bd4ba68d9d62bdfe65dc293c68377b7d3aa6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188031"
---
# <span data-ttu-id="6fe51-101">Remove-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6fe51-101">Remove-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="6fe51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fe51-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe51-103">Rimuove un database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="6fe51-103">Removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="6fe51-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6fe51-104">SYNTAX</span></span>

### <span data-ttu-id="6fe51-105">RemoveInstanceDatabaseFromInputParameters (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6fe51-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fe51-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="6fe51-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fe51-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="6fe51-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fe51-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6fe51-108">DESCRIPTION</span></span>
<span data-ttu-id="6fe51-109">Il cmdlet **Remove-AzSqlInstanceDatabase** rimuove un database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="6fe51-109">The **Remove-AzSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="6fe51-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6fe51-110">EXAMPLES</span></span>

### <span data-ttu-id="6fe51-111">Esempio 1: Rimuovere un database da un'istanza</span><span class="sxs-lookup"><span data-stu-id="6fe51-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6fe51-112">Questo comando rimuove il database denominato Database01 dall'istanza managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="6fe51-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="6fe51-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fe51-113">PARAMETERS</span></span>

### <span data-ttu-id="6fe51-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe51-114">-DefaultProfile</span></span>
<span data-ttu-id="6fe51-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6fe51-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fe51-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6fe51-116">-Force</span></span>
<span data-ttu-id="6fe51-117">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="6fe51-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6fe51-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fe51-118">-InputObject</span></span>
<span data-ttu-id="6fe51-119">L'oggetto Database di istanza da rimuovere</span><span class="sxs-lookup"><span data-stu-id="6fe51-119">The Instance Database object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe51-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6fe51-120">-InstanceName</span></span>
<span data-ttu-id="6fe51-121">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="6fe51-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe51-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6fe51-122">-Name</span></span>
<span data-ttu-id="6fe51-123">Nome del database delle istanze SQL Azure da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6fe51-123">The name of the Azure SQL Instance Database to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe51-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe51-124">-ResourceGroupName</span></span>
<span data-ttu-id="6fe51-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6fe51-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe51-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fe51-126">-ResourceId</span></span>
<span data-ttu-id="6fe51-127">ID risorsa dell'oggetto database dell'istanza da rimuovere</span><span class="sxs-lookup"><span data-stu-id="6fe51-127">The resource id of Instance Database object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fe51-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6fe51-128">-Confirm</span></span>
<span data-ttu-id="6fe51-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fe51-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fe51-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fe51-130">-WhatIf</span></span>
<span data-ttu-id="6fe51-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6fe51-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fe51-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6fe51-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fe51-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe51-133">CommonParameters</span></span>
<span data-ttu-id="6fe51-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fe51-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe51-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6fe51-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe51-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="6fe51-136">INPUTS</span></span>

### <span data-ttu-id="6fe51-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="6fe51-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="6fe51-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6fe51-138">System.String</span></span>

## <span data-ttu-id="6fe51-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6fe51-139">OUTPUTS</span></span>

### <span data-ttu-id="6fe51-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="6fe51-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="6fe51-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="6fe51-141">NOTES</span></span>

## <span data-ttu-id="6fe51-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6fe51-142">RELATED LINKS</span></span>
