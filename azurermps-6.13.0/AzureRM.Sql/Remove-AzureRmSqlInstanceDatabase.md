---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: f391dbb5d3e70e486a91c1dbb9e6517936bd2b3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520141"
---
# <span data-ttu-id="cdf19-101">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cdf19-101">Remove-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="cdf19-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cdf19-102">SYNOPSIS</span></span>
<span data-ttu-id="cdf19-103">Rimuove un database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="cdf19-103">Removes an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdf19-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdf19-104">SYNTAX</span></span>

### <span data-ttu-id="cdf19-105">RemoveInstanceDatabaseFromInputParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cdf19-105">RemoveInstanceDatabaseFromInputParameters (Default)</span></span>
```
Remove-AzureRmSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdf19-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="cdf19-106">RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Remove-AzureRmSqlInstanceDatabase [-InputObject] <AzureSqlManagedDatabaseModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdf19-107">RemoveInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="cdf19-107">RemoveInstanceDatabaseFromAzureResourceId</span></span>
```
Remove-AzureRmSqlInstanceDatabase [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdf19-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdf19-108">DESCRIPTION</span></span>
<span data-ttu-id="cdf19-109">Il cmdlet **Remove-AzureRmSqlInstanceDatabase** rimuove un database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="cdf19-109">The **Remove-AzureRmSqlInstanceDatabase** cmdlet removes an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="cdf19-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdf19-110">EXAMPLES</span></span>

### <span data-ttu-id="cdf19-111">Esempio 1: rimuovere un database da un'istanza</span><span class="sxs-lookup"><span data-stu-id="cdf19-111">Example 1: Remove a database from an instance</span></span>
```
PS C:\>Remove-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cdf19-112">Questo comando rimuove il database denominato Database01 dall'istanza managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="cdf19-112">This command removes the database named Database01 from instance managedInstance1.</span></span>

## <span data-ttu-id="cdf19-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cdf19-113">PARAMETERS</span></span>

### <span data-ttu-id="cdf19-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdf19-114">-DefaultProfile</span></span>
<span data-ttu-id="cdf19-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cdf19-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf19-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cdf19-116">-Force</span></span>
<span data-ttu-id="cdf19-117">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="cdf19-117">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf19-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdf19-118">-InputObject</span></span>
<span data-ttu-id="cdf19-119">Oggetto database dell'istanza da rimuovere</span><span class="sxs-lookup"><span data-stu-id="cdf19-119">The Instance Database object to remove</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: RemoveInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdf19-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="cdf19-120">-InstanceName</span></span>
<span data-ttu-id="cdf19-121">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="cdf19-121">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf19-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="cdf19-122">-Name</span></span>
<span data-ttu-id="cdf19-123">Nome del database dell'istanza SQL di Azure da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="cdf19-123">The name of the Azure SQL Instance Database to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf19-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdf19-124">-ResourceGroupName</span></span>
<span data-ttu-id="cdf19-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cdf19-125">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf19-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdf19-126">-ResourceId</span></span>
<span data-ttu-id="cdf19-127">ID risorsa dell'oggetto di database di istanza da rimuovere</span><span class="sxs-lookup"><span data-stu-id="cdf19-127">The resource id of Instance Database object to remove</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdf19-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cdf19-128">-Confirm</span></span>
<span data-ttu-id="cdf19-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdf19-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf19-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdf19-130">-WhatIf</span></span>
<span data-ttu-id="cdf19-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdf19-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdf19-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdf19-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf19-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdf19-133">CommonParameters</span></span>
<span data-ttu-id="cdf19-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdf19-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdf19-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdf19-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdf19-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cdf19-136">INPUTS</span></span>

### <span data-ttu-id="cdf19-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cdf19-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>
<span data-ttu-id="cdf19-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cdf19-138">System.String</span></span>

## <span data-ttu-id="cdf19-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdf19-139">OUTPUTS</span></span>

### <span data-ttu-id="cdf19-140">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cdf19-140">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="cdf19-141">Note</span><span class="sxs-lookup"><span data-stu-id="cdf19-141">NOTES</span></span>

## <span data-ttu-id="cdf19-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdf19-142">RELATED LINKS</span></span>
