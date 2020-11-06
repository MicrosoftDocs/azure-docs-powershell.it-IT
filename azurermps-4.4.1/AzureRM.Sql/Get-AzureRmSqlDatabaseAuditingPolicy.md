---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: a6fe2e171338885af2367d6fec1cc3a97002b321
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521515"
---
# <span data-ttu-id="86a71-101">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="86a71-101">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="86a71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86a71-102">SYNOPSIS</span></span>
<span data-ttu-id="86a71-103">Ottiene i criteri di controllo di un database.</span><span class="sxs-lookup"><span data-stu-id="86a71-103">Gets the auditing policy of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86a71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86a71-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86a71-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86a71-105">DESCRIPTION</span></span>
<span data-ttu-id="86a71-106">Il cmdlet **Get-AzureRmSqlDatabaseAuditingPolicy** ottiene i criteri di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="86a71-106">The **Get-AzureRmSqlDatabaseAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL Database.</span></span>
<span data-ttu-id="86a71-107">Per usare il cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="86a71-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="86a71-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86a71-108">EXAMPLES</span></span>

### <span data-ttu-id="86a71-109">Esempio 1: ottenere i criteri di controllo di un database SQL di Azure con il controllo della tabella definito</span><span class="sxs-lookup"><span data-stu-id="86a71-109">Example 1: Get the auditing policy of an Azure SQL database with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
UseServerDefault       : Disabled
EventType              : {PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure...} 
TableIdentifier        : MyAuditTableName
FullAuditLogsTableName : SQLDBAuditLogsMyAuditTableName
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Table
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

### <span data-ttu-id="86a71-110">Esempio 2: ottenere i criteri di controllo di un database SQL di Azure con il controllo BLOB definito</span><span class="sxs-lookup"><span data-stu-id="86a71-110">Example 2: Get the auditing policy of an Azure SQL database with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
AuditAction            : {}
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...} 
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Blob
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="86a71-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86a71-111">PARAMETERS</span></span>

### <span data-ttu-id="86a71-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="86a71-112">-DatabaseName</span></span>
<span data-ttu-id="86a71-113">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="86a71-113">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a71-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86a71-114">-ResourceGroupName</span></span>
<span data-ttu-id="86a71-115">Specifica il nome del gruppo di risorse a cui è assegnato il database.</span><span class="sxs-lookup"><span data-stu-id="86a71-115">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a71-116">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="86a71-116">-ServerName</span></span>
<span data-ttu-id="86a71-117">Specifica il nome del server in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="86a71-117">Specifies the name of the server where the database is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a71-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="86a71-118">-Confirm</span></span>
<span data-ttu-id="86a71-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86a71-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a71-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86a71-120">-WhatIf</span></span>
<span data-ttu-id="86a71-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86a71-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86a71-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86a71-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a71-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86a71-123">-DefaultProfile</span></span>
<span data-ttu-id="86a71-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86a71-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a71-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86a71-125">CommonParameters</span></span>
<span data-ttu-id="86a71-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86a71-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86a71-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86a71-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86a71-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86a71-128">INPUTS</span></span>

## <span data-ttu-id="86a71-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86a71-129">OUTPUTS</span></span>

### <span data-ttu-id="86a71-130">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="86a71-130">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="86a71-131">Note</span><span class="sxs-lookup"><span data-stu-id="86a71-131">NOTES</span></span>

## <span data-ttu-id="86a71-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86a71-132">RELATED LINKS</span></span>

[<span data-ttu-id="86a71-133">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="86a71-133">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="86a71-134">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="86a71-134">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)



