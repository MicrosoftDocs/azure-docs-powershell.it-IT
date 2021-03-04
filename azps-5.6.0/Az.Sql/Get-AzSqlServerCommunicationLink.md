---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 20f0fe00486b6b81ec1600e518c42121f5369095
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982077"
---
# <span data-ttu-id="e8931-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e8931-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="e8931-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8931-102">SYNOPSIS</span></span>
<span data-ttu-id="e8931-103">Recupera i collegamenti di comunicazione per le transazioni di database di tipo elastico tra i server di database.</span><span class="sxs-lookup"><span data-stu-id="e8931-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="e8931-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8931-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8931-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e8931-105">DESCRIPTION</span></span>
<span data-ttu-id="e8931-106">Il cmdlet **Get-AzSqlServerCommunicationLink** ottiene collegamenti di comunicazione da server a server per le transazioni di database elastiche in Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="e8931-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="e8931-107">Specificare il nome di un collegamento di comunicazione del server per visualizzare le proprietà del collegamento.</span><span class="sxs-lookup"><span data-stu-id="e8931-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="e8931-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8931-108">EXAMPLES</span></span>

### <span data-ttu-id="e8931-109">Esempio 1: Ottenere tutti i collegamenti di comunicazione per un server</span><span class="sxs-lookup"><span data-stu-id="e8931-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="e8931-110">Questo comando recupera tutti i collegamenti di comunicazione da server a server per le transazioni di database di dimensioni elastiche per il server denominato ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="e8931-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="e8931-111">Esempio 2: Ottenere un collegamento di comunicazione specifico per un server</span><span class="sxs-lookup"><span data-stu-id="e8931-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="e8931-112">Questo comando recupera il collegamento di comunicazione tra server denominato Link01.</span><span class="sxs-lookup"><span data-stu-id="e8931-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="e8931-113">Esempio 3: Ottenere tutti i collegamenti di comunicazione per un server usando i filtri</span><span class="sxs-lookup"><span data-stu-id="e8931-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="e8931-114">Questo comando recupera tutti i collegamenti di comunicazione da server a server per le transazioni di database elastiche per il server denominato ContosoServer17 che iniziano con "Collegamento".</span><span class="sxs-lookup"><span data-stu-id="e8931-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="e8931-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8931-115">PARAMETERS</span></span>

### <span data-ttu-id="e8931-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8931-116">-DefaultProfile</span></span>
<span data-ttu-id="e8931-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e8931-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8931-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="e8931-118">-LinkName</span></span>
<span data-ttu-id="e8931-119">Specifica il nome del collegamento di comunicazione del server che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8931-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8931-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8931-120">-ResourceGroupName</span></span>
<span data-ttu-id="e8931-121">Specifica il nome del gruppo di risorse a cui appartiene il server specificato dal *parametro ServerName.*</span><span class="sxs-lookup"><span data-stu-id="e8931-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="e8931-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e8931-122">-ServerName</span></span>
<span data-ttu-id="e8931-123">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="e8931-123">Specifies the name of a server.</span></span>
<span data-ttu-id="e8931-124">Questo server contiene un collegamento di comunicazione che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="e8931-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e8931-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8931-125">-Confirm</span></span>
<span data-ttu-id="e8931-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8931-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8931-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8931-127">-WhatIf</span></span>
<span data-ttu-id="e8931-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8931-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8931-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8931-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8931-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8931-130">CommonParameters</span></span>
<span data-ttu-id="e8931-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8931-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8931-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e8931-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8931-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="e8931-133">INPUTS</span></span>

### <span data-ttu-id="e8931-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e8931-134">System.String</span></span>

## <span data-ttu-id="e8931-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8931-135">OUTPUTS</span></span>

### <span data-ttu-id="e8931-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="e8931-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="e8931-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="e8931-137">NOTES</span></span>
* <span data-ttu-id="e8931-138">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="e8931-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="e8931-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8931-139">RELATED LINKS</span></span>

[<span data-ttu-id="e8931-140">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e8931-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="e8931-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e8931-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="e8931-142">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="e8931-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
