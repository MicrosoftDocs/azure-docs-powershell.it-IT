---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: a12c9846b9e52d3c5e19c74b5a0f755acb27daf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512243"
---
# <span data-ttu-id="1d386-101">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="1d386-101">Get-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="1d386-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d386-102">SYNOPSIS</span></span>
<span data-ttu-id="1d386-103">Ottiene i criteri di controllo di un server SQL.</span><span class="sxs-lookup"><span data-stu-id="1d386-103">Gets the auditing policy of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d386-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d386-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d386-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d386-105">DESCRIPTION</span></span>
<span data-ttu-id="1d386-106">Il cmdlet **Get-AzureRmSqlServerAuditingPolicy** ottiene i criteri di controllo di un server SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d386-106">The **Get-AzureRmSqlServerAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="1d386-107">Specificare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="1d386-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="1d386-108">Questo cmdlet restituisce un criterio usato dai database SQL di Azure che sono entrambi definiti nell'Azure SQL Server specificato e usano i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="1d386-108">This cmdlet returns a policy that is used by the Azure SQL databases that are both defined in the specified Azure SQL server and use its auditing policy.</span></span>

## <span data-ttu-id="1d386-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d386-109">EXAMPLES</span></span>

### <span data-ttu-id="1d386-110">Esempio 1: ottenere i criteri di controllo di un server SQL di Azure con il controllo della tabella definito</span><span class="sxs-lookup"><span data-stu-id="1d386-110">Example 1: Get the auditing policy of an Azure SQL server with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

### <span data-ttu-id="1d386-111">Esempio 2: ottenere i criteri di controllo di un server SQL di Azure con il controllo BLOB definito</span><span class="sxs-lookup"><span data-stu-id="1d386-111">Example 2: Get the auditing policy of an Azure SQL server with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

## <span data-ttu-id="1d386-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d386-112">PARAMETERS</span></span>

### <span data-ttu-id="1d386-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d386-113">-DefaultProfile</span></span>
<span data-ttu-id="1d386-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1d386-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d386-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d386-115">-ResourceGroupName</span></span>
<span data-ttu-id="1d386-116">Specifica il nome del gruppo di risorse a cui è assegnato Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1d386-116">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="1d386-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="1d386-117">-ServerName</span></span>
<span data-ttu-id="1d386-118">Specifica il nome di Azure SQL Server per cui questo cmdlet ottiene i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="1d386-118">Specifies the name of the Azure SQL server for which this cmdlet gets the auditing policy.</span></span>

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

### <span data-ttu-id="1d386-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1d386-119">-Confirm</span></span>
<span data-ttu-id="1d386-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d386-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d386-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d386-121">-WhatIf</span></span>
<span data-ttu-id="1d386-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d386-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d386-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d386-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d386-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d386-124">CommonParameters</span></span>
<span data-ttu-id="1d386-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d386-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d386-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d386-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d386-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d386-127">INPUTS</span></span>

### <span data-ttu-id="1d386-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1d386-128">None</span></span>
<span data-ttu-id="1d386-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1d386-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1d386-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d386-130">OUTPUTS</span></span>

### <span data-ttu-id="1d386-131">Microsoft. Azure. Commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="1d386-131">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="1d386-132">Note</span><span class="sxs-lookup"><span data-stu-id="1d386-132">NOTES</span></span>

## <span data-ttu-id="1d386-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d386-133">RELATED LINKS</span></span>

[<span data-ttu-id="1d386-134">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="1d386-134">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="1d386-135">Usare-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="1d386-135">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="1d386-136">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="1d386-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


