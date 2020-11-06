---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D3BA6534-CAAC-41E2-8442-0606B712E2B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 3fb40be93a1591e0337ec438e5eb3a317a08009b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512220"
---
# <span data-ttu-id="890e4-101">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="890e4-101">Remove-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="890e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="890e4-102">SYNOPSIS</span></span>
<span data-ttu-id="890e4-103">Rimuove il controllo di un database.</span><span class="sxs-lookup"><span data-stu-id="890e4-103">Removes the auditing of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="890e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="890e4-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseAuditing [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="890e4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="890e4-105">DESCRIPTION</span></span>
<span data-ttu-id="890e4-106">Il cmdlet **Remove-AzureRmSqlDatabaseAuditing** rimuove il controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="890e4-106">The **Remove-AzureRmSqlDatabaseAuditing** cmdlet removes the auditing of an Azure SQL database.</span></span>
<span data-ttu-id="890e4-107">Per usare questo cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="890e4-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="890e4-108">Dopo l'esecuzione di questo cmdlet, il controllo del database non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="890e4-108">After you run this cmdlet, auditing of the database is not performed.</span></span>
<span data-ttu-id="890e4-109">Se il comando riesce ed è stato usato il parametro *PassThru* , il cmdlet restituisce un oggetto che descrive il criterio di controllo corrente, oltre agli identificatori del database.</span><span class="sxs-lookup"><span data-stu-id="890e4-109">If the command succeeds and you have used the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, in addition to the database identifiers.</span></span>
<span data-ttu-id="890e4-110">Gli identificatori di database includono, ma non sono limitati a, **ResourceGroupName** , **nomeserver** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="890e4-110">Database identifiers include, but are not limited to, the **ResourceGroupName** , **ServerName** and **DatabaseName**.</span></span>

<span data-ttu-id="890e4-111">Se si rimuove il controllo di un database SQL di Azure, viene rimosso anche il rilevamento delle minacce.</span><span class="sxs-lookup"><span data-stu-id="890e4-111">If you remove auditing of an Azure SQL database, threat detection is also removed.</span></span>

<span data-ttu-id="890e4-112">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="890e4-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="890e4-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="890e4-113">EXAMPLES</span></span>

### <span data-ttu-id="890e4-114">Esempio 1: rimuovere il controllo di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="890e4-114">Example 1: Remove the auditing of an Azure SQL database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="890e4-115">Questo comando rimuove il controllo del database denominato Database01.</span><span class="sxs-lookup"><span data-stu-id="890e4-115">This command removes the auditing of database named Database01.</span></span>
<span data-ttu-id="890e4-116">Tale database si trova in Server01, assegnato al gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="890e4-116">That database is located on Server01, which is assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="890e4-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="890e4-117">PARAMETERS</span></span>

### <span data-ttu-id="890e4-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="890e4-118">-DatabaseName</span></span>
<span data-ttu-id="890e4-119">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="890e4-119">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="890e4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="890e4-120">-DefaultProfile</span></span>
<span data-ttu-id="890e4-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="890e4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="890e4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="890e4-122">-PassThru</span></span>
<span data-ttu-id="890e4-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="890e4-123">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="890e4-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="890e4-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="890e4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="890e4-125">-ResourceGroupName</span></span>
<span data-ttu-id="890e4-126">Specifica il nome del gruppo di risorse che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="890e4-126">Specifies the name of the resource group containing the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="890e4-127">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="890e4-127">-ServerName</span></span>
<span data-ttu-id="890e4-128">Specifica il nome del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="890e4-128">Specifies the name of the server containing the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="890e4-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="890e4-129">-Confirm</span></span>
<span data-ttu-id="890e4-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="890e4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="890e4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="890e4-131">-WhatIf</span></span>
<span data-ttu-id="890e4-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="890e4-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="890e4-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="890e4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="890e4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="890e4-134">CommonParameters</span></span>
<span data-ttu-id="890e4-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="890e4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="890e4-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="890e4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="890e4-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="890e4-137">INPUTS</span></span>

### <span data-ttu-id="890e4-138">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="890e4-138">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="890e4-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="890e4-139">OUTPUTS</span></span>

### <span data-ttu-id="890e4-140">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="890e4-140">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="890e4-141">Note</span><span class="sxs-lookup"><span data-stu-id="890e4-141">NOTES</span></span>

## <span data-ttu-id="890e4-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="890e4-142">RELATED LINKS</span></span>

[<span data-ttu-id="890e4-143">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="890e4-143">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="890e4-144">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="890e4-144">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="890e4-145">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="890e4-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


