---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 355690129f8edcda2586d2dfee570254ce44d998
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176903"
---
# <span data-ttu-id="e187e-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e187e-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="e187e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e187e-102">SYNOPSIS</span></span>
<span data-ttu-id="e187e-103">Recupera i collegamenti di comunicazione per le transazioni di database di tipo elastico tra server di database.</span><span class="sxs-lookup"><span data-stu-id="e187e-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="e187e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e187e-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e187e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e187e-105">DESCRIPTION</span></span>
<span data-ttu-id="e187e-106">Il cmdlet **Get-AzSqlServerCommunicationLink** ottiene collegamenti di comunicazione da server a server per le transazioni di database elastiche in Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="e187e-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="e187e-107">Specificare il nome di un collegamento di comunicazione del server per visualizzare le proprietà del collegamento.</span><span class="sxs-lookup"><span data-stu-id="e187e-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="e187e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e187e-108">EXAMPLES</span></span>

### <span data-ttu-id="e187e-109">Esempio 1: Ottenere tutti i collegamenti di comunicazione per un server</span><span class="sxs-lookup"><span data-stu-id="e187e-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="e187e-110">Questo comando recupera tutti i collegamenti di comunicazione da server a server per le transazioni di database di dimensioni elastiche per il server denominato ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="e187e-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="e187e-111">Esempio 2: Ottenere un collegamento di comunicazione specifico per un server</span><span class="sxs-lookup"><span data-stu-id="e187e-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="e187e-112">Questo comando recupera il collegamento di comunicazione da server a server denominato Link01.</span><span class="sxs-lookup"><span data-stu-id="e187e-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="e187e-113">Esempio 3: Ottenere tutti i collegamenti di comunicazione per un server usando i filtri</span><span class="sxs-lookup"><span data-stu-id="e187e-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="e187e-114">Questo comando recupera tutti i collegamenti di comunicazione da server a server per le transazioni di database elastiche per il server denominato ContosoServer17 che iniziano con "Collegamento".</span><span class="sxs-lookup"><span data-stu-id="e187e-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="e187e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e187e-115">PARAMETERS</span></span>

### <span data-ttu-id="e187e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e187e-116">-DefaultProfile</span></span>
<span data-ttu-id="e187e-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e187e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e187e-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="e187e-118">-LinkName</span></span>
<span data-ttu-id="e187e-119">Specifica il nome del collegamento di comunicazione del server che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e187e-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e187e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e187e-120">-ResourceGroupName</span></span>
<span data-ttu-id="e187e-121">Specifica il nome del gruppo di risorse a cui appartiene il server specificato dal *parametro ServerName.*</span><span class="sxs-lookup"><span data-stu-id="e187e-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="e187e-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e187e-122">-ServerName</span></span>
<span data-ttu-id="e187e-123">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="e187e-123">Specifies the name of a server.</span></span>
<span data-ttu-id="e187e-124">Questo server contiene un collegamento di comunicazione che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="e187e-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e187e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e187e-125">-Confirm</span></span>
<span data-ttu-id="e187e-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e187e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e187e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e187e-127">-WhatIf</span></span>
<span data-ttu-id="e187e-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e187e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e187e-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e187e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e187e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e187e-130">CommonParameters</span></span>
<span data-ttu-id="e187e-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e187e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e187e-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e187e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e187e-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="e187e-133">INPUTS</span></span>

### <span data-ttu-id="e187e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e187e-134">System.String</span></span>

## <span data-ttu-id="e187e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e187e-135">OUTPUTS</span></span>

### <span data-ttu-id="e187e-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="e187e-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="e187e-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="e187e-137">NOTES</span></span>
* <span data-ttu-id="e187e-138">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="e187e-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="e187e-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e187e-139">RELATED LINKS</span></span>

[<span data-ttu-id="e187e-140">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e187e-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="e187e-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="e187e-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="e187e-142">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="e187e-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
