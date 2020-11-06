---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 9058863da0af6addd243f5e7ec544a8dad7b3b03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507911"
---
# <span data-ttu-id="b04b0-101">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="b04b0-101">Get-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="b04b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b04b0-102">SYNOPSIS</span></span>
<span data-ttu-id="b04b0-103">Ottiene le impostazioni di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b04b0-103">Gets the auditing settings of an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b04b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b04b0-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditing [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b04b0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b04b0-105">DESCRIPTION</span></span>
<span data-ttu-id="b04b0-106">Il cmdlet **Get-AzureRmSqlDatabaseAuditing** ottiene le impostazioni di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b04b0-106">The **Get-AzureRmSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="b04b0-107">Per usare il cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="b04b0-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="b04b0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b04b0-108">EXAMPLES</span></span>

### <span data-ttu-id="b04b0-109">Esempio 1: recuperare le impostazioni di controllo di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="b04b0-109">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
AuditAction            : {}
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...}
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="b04b0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b04b0-110">PARAMETERS</span></span>

### <span data-ttu-id="b04b0-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b04b0-111">-DatabaseName</span></span>
<span data-ttu-id="b04b0-112">Nome database SQL.</span><span class="sxs-lookup"><span data-stu-id="b04b0-112">SQL Database name.</span></span>

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

### <span data-ttu-id="b04b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b04b0-113">-DefaultProfile</span></span>
<span data-ttu-id="b04b0-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b04b0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b04b0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b04b0-115">-ResourceGroupName</span></span>
<span data-ttu-id="b04b0-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b04b0-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="b04b0-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b04b0-117">-ServerName</span></span>
<span data-ttu-id="b04b0-118">Nome del server database SQL.</span><span class="sxs-lookup"><span data-stu-id="b04b0-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="b04b0-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b04b0-119">-Confirm</span></span>
<span data-ttu-id="b04b0-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b04b0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b04b0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b04b0-121">-WhatIf</span></span>
<span data-ttu-id="b04b0-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b04b0-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b04b0-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b04b0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b04b0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b04b0-124">CommonParameters</span></span>
<span data-ttu-id="b04b0-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b04b0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b04b0-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b04b0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b04b0-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b04b0-127">INPUTS</span></span>

### <span data-ttu-id="b04b0-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b04b0-128">None</span></span>
<span data-ttu-id="b04b0-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b04b0-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b04b0-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b04b0-130">OUTPUTS</span></span>

### <span data-ttu-id="b04b0-131">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="b04b0-131">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="b04b0-132">Note</span><span class="sxs-lookup"><span data-stu-id="b04b0-132">NOTES</span></span>

## <span data-ttu-id="b04b0-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b04b0-133">RELATED LINKS</span></span>
