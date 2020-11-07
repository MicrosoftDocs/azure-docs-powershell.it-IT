---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: 09aa7daaa3a583e42481e29675a08e8e1dd94d3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676801"
---
# <span data-ttu-id="40698-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="40698-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="40698-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40698-102">SYNOPSIS</span></span>
<span data-ttu-id="40698-103">Rimuove un'istanza di database gestito di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="40698-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="40698-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40698-104">SYNTAX</span></span>

### <span data-ttu-id="40698-105">RemoveInstanceFromInputParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="40698-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40698-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="40698-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40698-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="40698-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40698-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40698-108">DESCRIPTION</span></span>
<span data-ttu-id="40698-109">Il cmdlet **Remove-AzSqlInstance** rimuove un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="40698-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="40698-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40698-110">EXAMPLES</span></span>

### <span data-ttu-id="40698-111">Esempio 1: Rimuovi istanza</span><span class="sxs-lookup"><span data-stu-id="40698-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="40698-112">Questo comando rimuove l'istanza denominata managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="40698-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="40698-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40698-113">PARAMETERS</span></span>

### <span data-ttu-id="40698-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40698-114">-DefaultProfile</span></span>
<span data-ttu-id="40698-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40698-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40698-116">-Force</span><span class="sxs-lookup"><span data-stu-id="40698-116">-Force</span></span>
<span data-ttu-id="40698-117">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="40698-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="40698-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40698-118">-InputObject</span></span>
<span data-ttu-id="40698-119">Oggetto AzureSqlManagedInstanceModel da rimuovere</span><span class="sxs-lookup"><span data-stu-id="40698-119">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="40698-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="40698-120">-Name</span></span>
<span data-ttu-id="40698-121">Nome dell'istanza SQL.</span><span class="sxs-lookup"><span data-stu-id="40698-121">SQL instance name.</span></span>

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

### <span data-ttu-id="40698-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40698-122">-ResourceGroupName</span></span>
<span data-ttu-id="40698-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="40698-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="40698-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40698-124">-ResourceId</span></span>
<span data-ttu-id="40698-125">ID risorsa dell'oggetto Instance da rimuovere</span><span class="sxs-lookup"><span data-stu-id="40698-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="40698-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="40698-126">-Confirm</span></span>
<span data-ttu-id="40698-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40698-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40698-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40698-128">-WhatIf</span></span>
<span data-ttu-id="40698-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40698-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40698-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40698-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40698-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40698-131">CommonParameters</span></span>
<span data-ttu-id="40698-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40698-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40698-133">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40698-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40698-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40698-134">INPUTS</span></span>

### <span data-ttu-id="40698-135">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="40698-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="40698-136">System. String</span><span class="sxs-lookup"><span data-stu-id="40698-136">System.String</span></span>

## <span data-ttu-id="40698-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40698-137">OUTPUTS</span></span>

### <span data-ttu-id="40698-138">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="40698-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="40698-139">Note</span><span class="sxs-lookup"><span data-stu-id="40698-139">NOTES</span></span>

## <span data-ttu-id="40698-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40698-140">RELATED LINKS</span></span>
