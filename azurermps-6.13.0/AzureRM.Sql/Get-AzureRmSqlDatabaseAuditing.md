---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: b78bcf228012edd022f9551a5834c61cebc8d278
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518535"
---
# <span data-ttu-id="fdef2-101">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="fdef2-101">Get-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="fdef2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fdef2-102">SYNOPSIS</span></span>
<span data-ttu-id="fdef2-103">Ottiene le impostazioni di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="fdef2-103">Gets the auditing settings of an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdef2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdef2-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditing [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdef2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdef2-105">DESCRIPTION</span></span>
<span data-ttu-id="fdef2-106">Il cmdlet **Get-AzureRmSqlDatabaseAuditing** ottiene le impostazioni di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="fdef2-106">The **Get-AzureRmSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="fdef2-107">Per usare il cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="fdef2-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="fdef2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdef2-108">EXAMPLES</span></span>

### <span data-ttu-id="fdef2-109">Esempio 1: recuperare le impostazioni di controllo di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="fdef2-109">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

## <span data-ttu-id="fdef2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fdef2-110">PARAMETERS</span></span>

### <span data-ttu-id="fdef2-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fdef2-111">-DatabaseName</span></span>
<span data-ttu-id="fdef2-112">Nome database SQL.</span><span class="sxs-lookup"><span data-stu-id="fdef2-112">SQL Database name.</span></span>

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

### <span data-ttu-id="fdef2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdef2-113">-DefaultProfile</span></span>
<span data-ttu-id="fdef2-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fdef2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdef2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdef2-115">-ResourceGroupName</span></span>
<span data-ttu-id="fdef2-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fdef2-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="fdef2-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="fdef2-117">-ServerName</span></span>
<span data-ttu-id="fdef2-118">Nome del server database SQL.</span><span class="sxs-lookup"><span data-stu-id="fdef2-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="fdef2-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fdef2-119">-Confirm</span></span>
<span data-ttu-id="fdef2-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdef2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdef2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdef2-121">-WhatIf</span></span>
<span data-ttu-id="fdef2-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdef2-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdef2-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdef2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdef2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdef2-124">CommonParameters</span></span>
<span data-ttu-id="fdef2-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdef2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdef2-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdef2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdef2-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fdef2-127">INPUTS</span></span>

## <span data-ttu-id="fdef2-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdef2-128">OUTPUTS</span></span>

### <span data-ttu-id="fdef2-129">Microsoft. Azure. Commands. SQL. auditing. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="fdef2-129">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="fdef2-130">Note</span><span class="sxs-lookup"><span data-stu-id="fdef2-130">NOTES</span></span>

## <span data-ttu-id="fdef2-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdef2-131">RELATED LINKS</span></span>