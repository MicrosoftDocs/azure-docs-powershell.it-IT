---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 8027af33b9ea4f4184c10963da69e8be3b4e3961
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857346"
---
# <span data-ttu-id="294a2-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="294a2-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="294a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="294a2-102">SYNOPSIS</span></span>
<span data-ttu-id="294a2-103">Rimuove un gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="294a2-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="294a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="294a2-104">SYNTAX</span></span>

### <span data-ttu-id="294a2-105">RemoveIFGDefault (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="294a2-105">RemoveIFGDefault (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="294a2-106">Rimuovere un gruppo di failover dell'istanza dall'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="294a2-106">Remove a Instance Failover Group from Resource Id</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="294a2-107">Rimuovere un gruppo di failover di istanza dalla definizione dell'istanza di AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="294a2-107">Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="294a2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="294a2-108">DESCRIPTION</span></span>
<span data-ttu-id="294a2-109">Questo comando rimuove il gruppo di failover dell'istanza con il nome specificato, lasciando intatti tutti i database.</span><span class="sxs-lookup"><span data-stu-id="294a2-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="294a2-110">L'endpoint del listener verrà annullata la registrazione dal DNS.</span><span class="sxs-lookup"><span data-stu-id="294a2-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="294a2-111">L'area principale del gruppo di failover dell'istanza deve essere usata per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="294a2-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="294a2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="294a2-112">EXAMPLES</span></span>

### <span data-ttu-id="294a2-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="294a2-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="294a2-114">Rimuovere un gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="294a2-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="294a2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="294a2-115">PARAMETERS</span></span>

### <span data-ttu-id="294a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="294a2-116">-DefaultProfile</span></span>
<span data-ttu-id="294a2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="294a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="294a2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="294a2-118">-Force</span></span>
<span data-ttu-id="294a2-119">Ignorare il messaggio di conferma per l'esecuzione dell'azione.</span><span class="sxs-lookup"><span data-stu-id="294a2-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="294a2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="294a2-120">-InputObject</span></span>
<span data-ttu-id="294a2-121">Oggetto gruppo di failover dell'istanza da rimuovere</span><span class="sxs-lookup"><span data-stu-id="294a2-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="294a2-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="294a2-122">-Location</span></span>
<span data-ttu-id="294a2-123">Nome dell'area geografica locale da cui recuperare il gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="294a2-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault, Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="294a2-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="294a2-124">-Name</span></span>
<span data-ttu-id="294a2-125">Nome del gruppo di failover dell'istanza da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="294a2-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="294a2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="294a2-126">-ResourceGroupName</span></span>
<span data-ttu-id="294a2-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="294a2-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="294a2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="294a2-128">-ResourceId</span></span>
<span data-ttu-id="294a2-129">ID risorsa del gruppo di failover delle istanze da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="294a2-129">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="294a2-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="294a2-130">-Confirm</span></span>
<span data-ttu-id="294a2-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="294a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="294a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="294a2-132">-WhatIf</span></span>
<span data-ttu-id="294a2-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="294a2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="294a2-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="294a2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="294a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="294a2-135">CommonParameters</span></span>
<span data-ttu-id="294a2-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="294a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="294a2-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="294a2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="294a2-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="294a2-138">INPUTS</span></span>

### <span data-ttu-id="294a2-139">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="294a2-139">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="294a2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="294a2-140">System.String</span></span>

## <span data-ttu-id="294a2-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="294a2-141">OUTPUTS</span></span>

### <span data-ttu-id="294a2-142">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="294a2-142">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="294a2-143">Note</span><span class="sxs-lookup"><span data-stu-id="294a2-143">NOTES</span></span>

## <span data-ttu-id="294a2-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="294a2-144">RELATED LINKS</span></span>
