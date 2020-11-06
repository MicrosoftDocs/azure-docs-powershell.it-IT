---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 692D0B64-95EB-4D36-975F-65674B3B2F8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
ms.openlocfilehash: bd5d8d2c63b10ecc4aaabd5e96ab1ce844602325
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514079"
---
# <span data-ttu-id="da3f5-101">Remove-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="da3f5-101">Remove-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="da3f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da3f5-102">SYNOPSIS</span></span>
<span data-ttu-id="da3f5-103">Rimuove il controllo di un server SQL.</span><span class="sxs-lookup"><span data-stu-id="da3f5-103">Removes the auditing of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da3f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da3f5-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerAuditing [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da3f5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da3f5-105">DESCRIPTION</span></span>
<span data-ttu-id="da3f5-106">Il cmdlet **Remove-AzureRmSqlServerAuditing** rimuove il controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="da3f5-106">The **Remove-AzureRmSqlServerAuditing** cmdlet removes the auditing of an Azure SQL server.</span></span>
<span data-ttu-id="da3f5-107">Per usare questo cmdlet, specificare i parametri *ResourceGroupName* e *ServerName* per identificare il server.</span><span class="sxs-lookup"><span data-stu-id="da3f5-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="da3f5-108">Dopo aver eseguito questo cmdlet, non viene eseguito il controllo dei database in Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="da3f5-108">After you run this cmdlet, auditing of the databases on the Azure SQL server is not performed.</span></span>
<span data-ttu-id="da3f5-109">Se il comando riesce e si specifica il parametro *PassThru* , il cmdlet restituisce un oggetto che descrive il criterio di controllo corrente e gli identificatori di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="da3f5-109">If the command succeeds, and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy and the Azure SQL server identifiers.</span></span>
<span data-ttu-id="da3f5-110">Gli identificatori del server includono **ResourceGroupName** e **ServerName**.</span><span class="sxs-lookup"><span data-stu-id="da3f5-110">Server identifiers include the **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="da3f5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da3f5-111">EXAMPLES</span></span>

### <span data-ttu-id="da3f5-112">Esempio 1: rimuovere il controllo di un server SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="da3f5-112">Example 1: Remove the auditing of an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="da3f5-113">Questo comando rimuove il controllo di tutti i database presenti in Server01 nel gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="da3f5-113">This command removes the auditing of all the databases located on Server01 in resource group.</span></span>

## <span data-ttu-id="da3f5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da3f5-114">PARAMETERS</span></span>

### <span data-ttu-id="da3f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da3f5-115">-DefaultProfile</span></span>
<span data-ttu-id="da3f5-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="da3f5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da3f5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da3f5-117">-PassThru</span></span>
<span data-ttu-id="da3f5-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="da3f5-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="da3f5-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="da3f5-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="da3f5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da3f5-120">-ResourceGroupName</span></span>
<span data-ttu-id="da3f5-121">Specifica il nome del gruppo di risorse a cui è assegnato Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="da3f5-121">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="da3f5-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="da3f5-122">-ServerName</span></span>
<span data-ttu-id="da3f5-123">Specifica il nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="da3f5-123">Specifies the name of the Azure SQL server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da3f5-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="da3f5-124">-Confirm</span></span>
<span data-ttu-id="da3f5-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da3f5-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3f5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da3f5-126">-WhatIf</span></span>
<span data-ttu-id="da3f5-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da3f5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da3f5-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da3f5-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da3f5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da3f5-129">CommonParameters</span></span>
<span data-ttu-id="da3f5-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da3f5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da3f5-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da3f5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da3f5-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da3f5-132">INPUTS</span></span>

### <span data-ttu-id="da3f5-133">Microsoft. Azure. Commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="da3f5-133">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="da3f5-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da3f5-134">OUTPUTS</span></span>

### <span data-ttu-id="da3f5-135">Microsoft. Azure. Commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="da3f5-135">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="da3f5-136">Note</span><span class="sxs-lookup"><span data-stu-id="da3f5-136">NOTES</span></span>

## <span data-ttu-id="da3f5-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da3f5-137">RELATED LINKS</span></span>

[<span data-ttu-id="da3f5-138">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="da3f5-138">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="da3f5-139">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="da3f5-139">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="da3f5-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="da3f5-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


