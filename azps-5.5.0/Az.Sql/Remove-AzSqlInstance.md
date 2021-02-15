---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: e361dc9a224649b7b1af38594145f14e24091d7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188926"
---
# <span data-ttu-id="36e2e-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="36e2e-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="36e2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="36e2e-103">Rimuove un'istanza di SQL gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="36e2e-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="36e2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36e2e-104">SYNTAX</span></span>

### <span data-ttu-id="36e2e-105">RemoveInstanceFromInputParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="36e2e-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36e2e-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="36e2e-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36e2e-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="36e2e-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36e2e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="36e2e-108">DESCRIPTION</span></span>
<span data-ttu-id="36e2e-109">Il cmdlet **Remove-AzSqlInstance** rimuove un'istanza gestita SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="36e2e-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="36e2e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36e2e-110">EXAMPLES</span></span>

### <span data-ttu-id="36e2e-111">Esempio 1: Rimuovere un'istanza</span><span class="sxs-lookup"><span data-stu-id="36e2e-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="36e2e-112">Questo comando rimuove l'istanza denominata managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="36e2e-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="36e2e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36e2e-113">PARAMETERS</span></span>

### <span data-ttu-id="36e2e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e2e-114">-DefaultProfile</span></span>
<span data-ttu-id="36e2e-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36e2e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36e2e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="36e2e-116">-Force</span></span>
<span data-ttu-id="36e2e-117">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="36e2e-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="36e2e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36e2e-118">-InputObject</span></span>
<span data-ttu-id="36e2e-119">Oggetto AzureSqlManagedInstanceModel da rimuovere</span><span class="sxs-lookup"><span data-stu-id="36e2e-119">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="36e2e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="36e2e-120">-Name</span></span>
<span data-ttu-id="36e2e-121">SQL di istanza.</span><span class="sxs-lookup"><span data-stu-id="36e2e-121">SQL instance name.</span></span>

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

### <span data-ttu-id="36e2e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36e2e-122">-ResourceGroupName</span></span>
<span data-ttu-id="36e2e-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="36e2e-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="36e2e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36e2e-124">-ResourceId</span></span>
<span data-ttu-id="36e2e-125">ID risorsa dell'oggetto istanza da rimuovere</span><span class="sxs-lookup"><span data-stu-id="36e2e-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="36e2e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36e2e-126">-Confirm</span></span>
<span data-ttu-id="36e2e-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36e2e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36e2e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36e2e-128">-WhatIf</span></span>
<span data-ttu-id="36e2e-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36e2e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36e2e-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36e2e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36e2e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e2e-131">CommonParameters</span></span>
<span data-ttu-id="36e2e-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36e2e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e2e-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36e2e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e2e-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="36e2e-134">INPUTS</span></span>

### <span data-ttu-id="36e2e-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="36e2e-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="36e2e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="36e2e-136">System.String</span></span>

## <span data-ttu-id="36e2e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36e2e-137">OUTPUTS</span></span>

### <span data-ttu-id="36e2e-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="36e2e-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="36e2e-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="36e2e-139">NOTES</span></span>

## <span data-ttu-id="36e2e-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36e2e-140">RELATED LINKS</span></span>
