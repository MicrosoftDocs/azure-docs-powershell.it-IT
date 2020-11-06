---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 8b0f66ceb624689ad66a9ab8fa4bbf9d0fcb2391
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509032"
---
# <span data-ttu-id="42ea9-101">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="42ea9-101">New-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="42ea9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="42ea9-103">Crea un collegamento di comunicazione per le transazioni di database elastiche tra due server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="42ea9-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42ea9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42ea9-104">SYNTAX</span></span>

```
New-AzureRmSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42ea9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42ea9-105">DESCRIPTION</span></span>
<span data-ttu-id="42ea9-106">Il cmdlet **New-AzureRmSqlServerCommunicationLink** crea un collegamento di comunicazione per le transazioni di database elastiche tra due server logici in database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="42ea9-106">The **New-AzureRmSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="42ea9-107">Le transazioni di database elastiche possono estendere i database in uno dei server associati.</span><span class="sxs-lookup"><span data-stu-id="42ea9-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="42ea9-108">È possibile creare più collegamenti in un server.</span><span class="sxs-lookup"><span data-stu-id="42ea9-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="42ea9-109">Di conseguenza, le transazioni di database elastiche possono essere estese in un numero maggiore di server.</span><span class="sxs-lookup"><span data-stu-id="42ea9-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="42ea9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42ea9-110">EXAMPLES</span></span>

### <span data-ttu-id="42ea9-111">Esempio 1: creare un collegamento di comunicazione</span><span class="sxs-lookup"><span data-stu-id="42ea9-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="42ea9-112">Questo comando crea un collegamento denominato Link01 tra ContosoServer17 e ContosoServer02.</span><span class="sxs-lookup"><span data-stu-id="42ea9-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="42ea9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42ea9-113">PARAMETERS</span></span>

### <span data-ttu-id="42ea9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42ea9-114">-AsJob</span></span>
<span data-ttu-id="42ea9-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="42ea9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42ea9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ea9-116">-DefaultProfile</span></span>
<span data-ttu-id="42ea9-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="42ea9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42ea9-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="42ea9-118">-LinkName</span></span>
<span data-ttu-id="42ea9-119">Specifica il nome del collegamento di comunicazione del server creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42ea9-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea9-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="42ea9-120">-PartnerServer</span></span>
<span data-ttu-id="42ea9-121">Specifica il nome dell'altro server che partecipa a questo collegamento di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="42ea9-121">Specifies the name of the other server that takes part in this communication link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ea9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42ea9-122">-ResourceGroupName</span></span>
<span data-ttu-id="42ea9-123">Specifica il nome del gruppo di risorse a cui appartiene il server specificato dal parametro *ServerName* .</span><span class="sxs-lookup"><span data-stu-id="42ea9-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="42ea9-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="42ea9-124">-ServerName</span></span>
<span data-ttu-id="42ea9-125">Specifica il nome del server in cui questo cmdlet configura il collegamento di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="42ea9-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="42ea9-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="42ea9-126">-Confirm</span></span>
<span data-ttu-id="42ea9-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42ea9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42ea9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42ea9-128">-WhatIf</span></span>
<span data-ttu-id="42ea9-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42ea9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42ea9-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42ea9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42ea9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ea9-131">CommonParameters</span></span>
<span data-ttu-id="42ea9-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42ea9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ea9-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42ea9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ea9-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42ea9-134">INPUTS</span></span>

### <span data-ttu-id="42ea9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="42ea9-135">System.String</span></span>

## <span data-ttu-id="42ea9-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42ea9-136">OUTPUTS</span></span>

### <span data-ttu-id="42ea9-137">Microsoft. Azure. Commands. SQL. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="42ea9-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="42ea9-138">Note</span><span class="sxs-lookup"><span data-stu-id="42ea9-138">NOTES</span></span>
* <span data-ttu-id="42ea9-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="42ea9-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="42ea9-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42ea9-140">RELATED LINKS</span></span>

[<span data-ttu-id="42ea9-141">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="42ea9-141">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="42ea9-142">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="42ea9-142">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="42ea9-143">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="42ea9-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
