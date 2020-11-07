---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: b2d4d5e86870bf0c69e506f387f6309dbcc8af7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857466"
---
# <span data-ttu-id="05b24-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="05b24-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="05b24-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05b24-102">SYNOPSIS</span></span>
<span data-ttu-id="05b24-103">Ottiene collegamenti di comunicazione per le transazioni di database elastici tra i server di database.</span><span class="sxs-lookup"><span data-stu-id="05b24-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="05b24-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05b24-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05b24-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05b24-105">DESCRIPTION</span></span>
<span data-ttu-id="05b24-106">Il cmdlet **Get-AzSqlServerCommunicationLink** ottiene collegamenti di comunicazione da server a server per le transazioni di database flessibili in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="05b24-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="05b24-107">Specificare il nome di un collegamento di comunicazione del server per visualizzare le proprietà del collegamento.</span><span class="sxs-lookup"><span data-stu-id="05b24-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="05b24-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05b24-108">EXAMPLES</span></span>

### <span data-ttu-id="05b24-109">Esempio 1: ottenere tutti i collegamenti di comunicazione per un server</span><span class="sxs-lookup"><span data-stu-id="05b24-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="05b24-110">Questo comando consente di ottenere tutti i collegamenti di comunicazione da server a server per le transazioni di database elastici per il server denominato ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="05b24-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="05b24-111">Esempio 2: ottenere un collegamento di comunicazione specifico per un server</span><span class="sxs-lookup"><span data-stu-id="05b24-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="05b24-112">Questo comando ottiene il collegamento di comunicazione da server a server denominato Link01.</span><span class="sxs-lookup"><span data-stu-id="05b24-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="05b24-113">Esempio 3: ottenere tutti i collegamenti di comunicazione per un server tramite filtro</span><span class="sxs-lookup"><span data-stu-id="05b24-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="05b24-114">Questo comando consente di ottenere tutti i collegamenti di comunicazione da server a server per le transazioni di database elastiche per il server denominato ContosoServer17 che iniziano con "collegamento".</span><span class="sxs-lookup"><span data-stu-id="05b24-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="05b24-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05b24-115">PARAMETERS</span></span>

### <span data-ttu-id="05b24-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05b24-116">-DefaultProfile</span></span>
<span data-ttu-id="05b24-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="05b24-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05b24-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="05b24-118">-LinkName</span></span>
<span data-ttu-id="05b24-119">Specifica il nome del collegamento di comunicazione del server ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05b24-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="05b24-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05b24-120">-ResourceGroupName</span></span>
<span data-ttu-id="05b24-121">Specifica il nome del gruppo di risorse a cui appartiene il server specificato dal parametro *ServerName* .</span><span class="sxs-lookup"><span data-stu-id="05b24-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="05b24-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="05b24-122">-ServerName</span></span>
<span data-ttu-id="05b24-123">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="05b24-123">Specifies the name of a server.</span></span>
<span data-ttu-id="05b24-124">Questo server contiene un collegamento di comunicazione che viene ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05b24-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="05b24-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="05b24-125">-Confirm</span></span>
<span data-ttu-id="05b24-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05b24-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05b24-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05b24-127">-WhatIf</span></span>
<span data-ttu-id="05b24-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05b24-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05b24-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05b24-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05b24-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05b24-130">CommonParameters</span></span>
<span data-ttu-id="05b24-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05b24-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05b24-132">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05b24-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05b24-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05b24-133">INPUTS</span></span>

### <span data-ttu-id="05b24-134">System. String</span><span class="sxs-lookup"><span data-stu-id="05b24-134">System.String</span></span>

## <span data-ttu-id="05b24-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05b24-135">OUTPUTS</span></span>

### <span data-ttu-id="05b24-136">Microsoft. Azure. Commands. SQL. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="05b24-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="05b24-137">Note</span><span class="sxs-lookup"><span data-stu-id="05b24-137">NOTES</span></span>
* <span data-ttu-id="05b24-138">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="05b24-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="05b24-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05b24-139">RELATED LINKS</span></span>

[<span data-ttu-id="05b24-140">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="05b24-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="05b24-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="05b24-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="05b24-142">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="05b24-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
