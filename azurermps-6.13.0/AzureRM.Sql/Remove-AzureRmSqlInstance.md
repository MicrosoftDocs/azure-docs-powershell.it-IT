---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlmanagedinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
ms.openlocfilehash: 1da1c431d41c7277a8291bb9a012218057b9c678
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520142"
---
# <span data-ttu-id="af8ce-101">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="af8ce-101">Remove-AzureRmSqlInstance</span></span>

## <span data-ttu-id="af8ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af8ce-102">SYNOPSIS</span></span>
<span data-ttu-id="af8ce-103">Rimuove un'istanza di database gestito di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="af8ce-103">Removes an Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af8ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af8ce-104">SYNTAX</span></span>

### <span data-ttu-id="af8ce-105">RemoveInstanceFromInputParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="af8ce-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af8ce-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="af8ce-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af8ce-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="af8ce-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzureRmSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af8ce-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af8ce-108">DESCRIPTION</span></span>
<span data-ttu-id="af8ce-109">Il cmdlet **Remove-AzureRmSqlInstance** rimuove un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="af8ce-109">The **Remove-AzureRmSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="af8ce-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af8ce-110">EXAMPLES</span></span>

### <span data-ttu-id="af8ce-111">Esempio 1: Rimuovi istanza</span><span class="sxs-lookup"><span data-stu-id="af8ce-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="af8ce-112">Questo comando rimuove l'istanza denominata managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="af8ce-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="af8ce-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af8ce-113">PARAMETERS</span></span>

### <span data-ttu-id="af8ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af8ce-114">-DefaultProfile</span></span>
<span data-ttu-id="af8ce-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af8ce-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af8ce-116">-Force</span><span class="sxs-lookup"><span data-stu-id="af8ce-116">-Force</span></span>
<span data-ttu-id="af8ce-117">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="af8ce-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="af8ce-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af8ce-118">-InputObject</span></span>
<span data-ttu-id="af8ce-119">Oggetto AzureSqlManagedInstanceModel da rimuovere</span><span class="sxs-lookup"><span data-stu-id="af8ce-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af8ce-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="af8ce-120">-Name</span></span>
<span data-ttu-id="af8ce-121">Nome dell'istanza SQL.</span><span class="sxs-lookup"><span data-stu-id="af8ce-121">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8ce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af8ce-122">-ResourceGroupName</span></span>
<span data-ttu-id="af8ce-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="af8ce-123">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af8ce-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af8ce-124">-ResourceId</span></span>
<span data-ttu-id="af8ce-125">ID risorsa dell'oggetto Instance da rimuovere</span><span class="sxs-lookup"><span data-stu-id="af8ce-125">The resource id of instance object to remove</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8ce-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af8ce-126">-Confirm</span></span>
<span data-ttu-id="af8ce-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af8ce-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af8ce-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af8ce-128">-WhatIf</span></span>
<span data-ttu-id="af8ce-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af8ce-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af8ce-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af8ce-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af8ce-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af8ce-131">CommonParameters</span></span>
<span data-ttu-id="af8ce-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af8ce-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af8ce-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af8ce-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af8ce-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af8ce-134">INPUTS</span></span>

### <span data-ttu-id="af8ce-135">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="af8ce-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="af8ce-136">System. String</span><span class="sxs-lookup"><span data-stu-id="af8ce-136">System.String</span></span>

## <span data-ttu-id="af8ce-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af8ce-137">OUTPUTS</span></span>

### <span data-ttu-id="af8ce-138">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="af8ce-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="af8ce-139">Note</span><span class="sxs-lookup"><span data-stu-id="af8ce-139">NOTES</span></span>

## <span data-ttu-id="af8ce-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af8ce-140">RELATED LINKS</span></span>