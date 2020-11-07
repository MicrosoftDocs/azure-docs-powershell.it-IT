---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 8240712b4ec6ef17dfff597bed4dc62d60be42b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685812"
---
# <span data-ttu-id="08e41-101">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="08e41-101">Get-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="08e41-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08e41-102">SYNOPSIS</span></span>
<span data-ttu-id="08e41-103">Ottiene collegamenti di comunicazione per le transazioni di database elastici tra i server di database.</span><span class="sxs-lookup"><span data-stu-id="08e41-103">Gets communication links for elastic database transactions between database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08e41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08e41-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08e41-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08e41-105">DESCRIPTION</span></span>
<span data-ttu-id="08e41-106">Il cmdlet **Get-AzureRmSqlServerCommunicationLink** ottiene collegamenti di comunicazione da server a server per le transazioni di database flessibili in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="08e41-106">The **Get-AzureRmSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="08e41-107">Specificare il nome di un collegamento di comunicazione del server per visualizzare le proprietà del collegamento.</span><span class="sxs-lookup"><span data-stu-id="08e41-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="08e41-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08e41-108">EXAMPLES</span></span>

### <span data-ttu-id="08e41-109">Esempio 1: ottenere tutti i collegamenti di comunicazione per un server</span><span class="sxs-lookup"><span data-stu-id="08e41-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="08e41-110">Questo comando consente di ottenere tutti i collegamenti di comunicazione da server a server per le transazioni di database elastici per il server denominato ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="08e41-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="08e41-111">Esempio 2: ottenere un collegamento di comunicazione specifico per un server</span><span class="sxs-lookup"><span data-stu-id="08e41-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="08e41-112">Questo comando ottiene il collegamento di comunicazione da server a server denominato Link01.</span><span class="sxs-lookup"><span data-stu-id="08e41-112">This command gets the server-to-server communication link named Link01.</span></span>

## <span data-ttu-id="08e41-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08e41-113">PARAMETERS</span></span>

### <span data-ttu-id="08e41-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e41-114">-DefaultProfile</span></span>
<span data-ttu-id="08e41-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="08e41-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08e41-116">-LinkName</span><span class="sxs-lookup"><span data-stu-id="08e41-116">-LinkName</span></span>
<span data-ttu-id="08e41-117">Specifica il nome del collegamento di comunicazione del server ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08e41-117">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08e41-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08e41-118">-ResourceGroupName</span></span>
<span data-ttu-id="08e41-119">Specifica il nome del gruppo di risorse a cui appartiene il server specificato dal parametro *ServerName* .</span><span class="sxs-lookup"><span data-stu-id="08e41-119">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="08e41-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="08e41-120">-ServerName</span></span>
<span data-ttu-id="08e41-121">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="08e41-121">Specifies the name of a server.</span></span>
<span data-ttu-id="08e41-122">Questo server contiene un collegamento di comunicazione che viene ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08e41-122">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="08e41-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="08e41-123">-Confirm</span></span>
<span data-ttu-id="08e41-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08e41-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08e41-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08e41-125">-WhatIf</span></span>
<span data-ttu-id="08e41-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08e41-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08e41-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08e41-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08e41-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e41-128">CommonParameters</span></span>
<span data-ttu-id="08e41-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08e41-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e41-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08e41-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e41-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08e41-131">INPUTS</span></span>

### <span data-ttu-id="08e41-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="08e41-132">None</span></span>
<span data-ttu-id="08e41-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="08e41-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="08e41-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08e41-134">OUTPUTS</span></span>

### <span data-ttu-id="08e41-135">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="08e41-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="08e41-136">Note</span><span class="sxs-lookup"><span data-stu-id="08e41-136">NOTES</span></span>
* <span data-ttu-id="08e41-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="08e41-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="08e41-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08e41-138">RELATED LINKS</span></span>

[<span data-ttu-id="08e41-139">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="08e41-139">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="08e41-140">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="08e41-140">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="08e41-141">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="08e41-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
