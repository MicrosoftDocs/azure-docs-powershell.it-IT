---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 79d920f866991cae15e2da08d03e2eecd4d2e91e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969773"
---
# <span data-ttu-id="c14d7-101">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="c14d7-101">New-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="c14d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c14d7-102">SYNOPSIS</span></span>
<span data-ttu-id="c14d7-103">Crea un collegamento di comunicazione per le transazioni di database elastiche tra due SQL server di database.</span><span class="sxs-lookup"><span data-stu-id="c14d7-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

## <span data-ttu-id="c14d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c14d7-104">SYNTAX</span></span>

```
New-AzSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c14d7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c14d7-105">DESCRIPTION</span></span>
<span data-ttu-id="c14d7-106">Il cmdlet **New-AzSqlServerCommunicationLink** crea un collegamento di comunicazione per le transazioni di database elastiche tra due server logici in Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="c14d7-106">The **New-AzSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="c14d7-107">Le transazioni di database di tipo elastico possono estendersi su database di uno dei server associati.</span><span class="sxs-lookup"><span data-stu-id="c14d7-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="c14d7-108">È possibile creare più collegamenti in un server.</span><span class="sxs-lookup"><span data-stu-id="c14d7-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="c14d7-109">Di conseguenza, le transazioni di database elastiche possono estendersi su un numero maggiore di server.</span><span class="sxs-lookup"><span data-stu-id="c14d7-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="c14d7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c14d7-110">EXAMPLES</span></span>

### <span data-ttu-id="c14d7-111">Esempio 1: Creare un collegamento di comunicazione</span><span class="sxs-lookup"><span data-stu-id="c14d7-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="c14d7-112">Questo comando crea un collegamento denominato Link01 tra ContosoServer17 e ContosoServer02.</span><span class="sxs-lookup"><span data-stu-id="c14d7-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="c14d7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c14d7-113">PARAMETERS</span></span>

### <span data-ttu-id="c14d7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c14d7-114">-AsJob</span></span>
<span data-ttu-id="c14d7-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c14d7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c14d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14d7-116">-DefaultProfile</span></span>
<span data-ttu-id="c14d7-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c14d7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14d7-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="c14d7-118">-LinkName</span></span>
<span data-ttu-id="c14d7-119">Specifica il nome del collegamento di comunicazione del server creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c14d7-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c14d7-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="c14d7-120">-PartnerServer</span></span>
<span data-ttu-id="c14d7-121">Specifica il nome dell'altro server che prende parte a questo collegamento di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="c14d7-121">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="c14d7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c14d7-122">-ResourceGroupName</span></span>
<span data-ttu-id="c14d7-123">Specifica il nome del gruppo di risorse a cui appartiene il server specificato dal *parametro ServerName.*</span><span class="sxs-lookup"><span data-stu-id="c14d7-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="c14d7-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c14d7-124">-ServerName</span></span>
<span data-ttu-id="c14d7-125">Specifica il nome del server in cui il cmdlet configura il collegamento di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="c14d7-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="c14d7-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c14d7-126">-Confirm</span></span>
<span data-ttu-id="c14d7-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c14d7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c14d7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c14d7-128">-WhatIf</span></span>
<span data-ttu-id="c14d7-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c14d7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c14d7-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c14d7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c14d7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14d7-131">CommonParameters</span></span>
<span data-ttu-id="c14d7-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c14d7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14d7-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c14d7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c14d7-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="c14d7-134">INPUTS</span></span>

### <span data-ttu-id="c14d7-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c14d7-135">System.String</span></span>

## <span data-ttu-id="c14d7-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c14d7-136">OUTPUTS</span></span>

### <span data-ttu-id="c14d7-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="c14d7-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="c14d7-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="c14d7-138">NOTES</span></span>
* <span data-ttu-id="c14d7-139">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="c14d7-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="c14d7-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c14d7-140">RELATED LINKS</span></span>

[<span data-ttu-id="c14d7-141">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="c14d7-141">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="c14d7-142">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="c14d7-142">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="c14d7-143">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="c14d7-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
