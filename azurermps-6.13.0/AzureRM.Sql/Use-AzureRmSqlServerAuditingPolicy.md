---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 381F5B34-983C-4733-B384-35D6579B79A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/use-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Use-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: a0dc151c86caf41131649f7e4e37ee60c6f19b01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517319"
---
# <span data-ttu-id="cb573-101">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="cb573-101">Use-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="cb573-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb573-102">SYNOPSIS</span></span>
<span data-ttu-id="cb573-103">Specifica che un database usa i criteri di controllo del server host.</span><span class="sxs-lookup"><span data-stu-id="cb573-103">Specifies that a database uses the auditing policy of its host server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb573-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb573-104">SYNTAX</span></span>

```
Use-AzureRmSqlServerAuditingPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb573-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb573-105">DESCRIPTION</span></span>
<span data-ttu-id="cb573-106">Il cmdlet **use-AzureRmSqlServerAuditingPolicy** specifica che un database usa i criteri di controllo del server host.</span><span class="sxs-lookup"><span data-stu-id="cb573-106">The **Use-AzureRmSqlServerAuditingPolicy** cmdlet specifies that a database uses the auditing policy of its host server.</span></span>
<span data-ttu-id="cb573-107">Specificare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="cb573-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="cb573-108">Se non è stato definito alcun criterio di controllo per il server di database, il cmdlet non riesce.</span><span class="sxs-lookup"><span data-stu-id="cb573-108">If no auditing policy is defined for the database server, this cmdlet fails.</span></span>
<span data-ttu-id="cb573-109">Se l'host usa il controllo a livello di server, il rilevamento delle minacce viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="cb573-109">If the host uses server level auditing, threat detection is removed.</span></span>

## <span data-ttu-id="cb573-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb573-110">EXAMPLES</span></span>

### <span data-ttu-id="cb573-111">Esempio 1: configurare un database per l'uso dei criteri di controllo del server</span><span class="sxs-lookup"><span data-stu-id="cb573-111">Example 1: Configure a database to use the auditing policy of its server</span></span>
```
PS C:\>Use-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server02" -DatabaseName "Database01"
```

<span data-ttu-id="cb573-112">Questo comando specifica che il database denominato Database01 in Server02 usa i criteri di controllo del server.</span><span class="sxs-lookup"><span data-stu-id="cb573-112">This command specifies that the database named Database01 on Server02 uses the auditing policy of the server.</span></span>

## <span data-ttu-id="cb573-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb573-113">PARAMETERS</span></span>

### <span data-ttu-id="cb573-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cb573-114">-DatabaseName</span></span>
<span data-ttu-id="cb573-115">Specifica il nome del database che utilizzerà i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="cb573-115">Specifies the name of the database that will use the auditing policy.</span></span>

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

### <span data-ttu-id="cb573-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb573-116">-DefaultProfile</span></span>
<span data-ttu-id="cb573-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cb573-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb573-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb573-118">-PassThru</span></span>
<span data-ttu-id="cb573-119">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="cb573-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cb573-120">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="cb573-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cb573-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb573-121">-ResourceGroupName</span></span>
<span data-ttu-id="cb573-122">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="cb573-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="cb573-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="cb573-123">-ServerName</span></span>
<span data-ttu-id="cb573-124">Specifica il nome del server che ospita il database che usa i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="cb573-124">Specifies the name of the server that hosts the database that uses the auditing policy.</span></span>

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

### <span data-ttu-id="cb573-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb573-125">CommonParameters</span></span>
<span data-ttu-id="cb573-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb573-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb573-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb573-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb573-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb573-128">INPUTS</span></span>

### <span data-ttu-id="cb573-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cb573-129">System.String</span></span>

## <span data-ttu-id="cb573-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb573-130">OUTPUTS</span></span>

### <span data-ttu-id="cb573-131">Microsoft. Azure. Commands. SQL. auditing. Model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="cb573-131">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="cb573-132">Note</span><span class="sxs-lookup"><span data-stu-id="cb573-132">NOTES</span></span>

## <span data-ttu-id="cb573-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb573-133">RELATED LINKS</span></span>

[<span data-ttu-id="cb573-134">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="cb573-134">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="cb573-135">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="cb573-135">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="cb573-136">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="cb573-136">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="cb573-137">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="cb573-137">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="cb573-138">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="cb573-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


