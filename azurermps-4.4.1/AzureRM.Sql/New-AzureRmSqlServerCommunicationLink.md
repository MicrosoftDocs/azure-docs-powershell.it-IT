---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: ac2ec676143ef1179adbfeb793bd787d81e8f435
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510252"
---
# <span data-ttu-id="2bb34-101">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="2bb34-101">New-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="2bb34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2bb34-102">SYNOPSIS</span></span>
<span data-ttu-id="2bb34-103">Crea un collegamento di comunicazione per le transazioni di database elastiche tra due server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="2bb34-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bb34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2bb34-104">SYNTAX</span></span>

```
New-AzureRmSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2bb34-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bb34-105">DESCRIPTION</span></span>
<span data-ttu-id="2bb34-106">Il cmdlet **New-AzureRmSqlServerCommunicationLink** crea un collegamento di comunicazione per le transazioni di database elastiche tra due server logici in database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="2bb34-106">The **New-AzureRmSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="2bb34-107">Le transazioni di database elastiche possono estendere i database in uno dei server associati.</span><span class="sxs-lookup"><span data-stu-id="2bb34-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="2bb34-108">È possibile creare più collegamenti in un server.</span><span class="sxs-lookup"><span data-stu-id="2bb34-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="2bb34-109">Di conseguenza, le transazioni di database elastiche possono essere estese in un numero maggiore di server.</span><span class="sxs-lookup"><span data-stu-id="2bb34-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="2bb34-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2bb34-110">EXAMPLES</span></span>

### <span data-ttu-id="2bb34-111">Esempio 1: creare un collegamento di comunicazione</span><span class="sxs-lookup"><span data-stu-id="2bb34-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="2bb34-112">Questo comando crea un collegamento denominato Link01 tra ContosoServer17 e ContosoServer02.</span><span class="sxs-lookup"><span data-stu-id="2bb34-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="2bb34-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2bb34-113">PARAMETERS</span></span>

### <span data-ttu-id="2bb34-114">-LinkName</span><span class="sxs-lookup"><span data-stu-id="2bb34-114">-LinkName</span></span>
<span data-ttu-id="2bb34-115">Specifica il nome del collegamento di comunicazione del server creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bb34-115">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2bb34-116">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="2bb34-116">-PartnerServer</span></span>
<span data-ttu-id="2bb34-117">Specifica il nome dell'altro server che partecipa a questo collegamento di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="2bb34-117">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="2bb34-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bb34-118">-ResourceGroupName</span></span>
<span data-ttu-id="2bb34-119">Specifica il nome del gruppo di risorse a cui appartiene il server specificato dal parametro *ServerName* .</span><span class="sxs-lookup"><span data-stu-id="2bb34-119">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="2bb34-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="2bb34-120">-ServerName</span></span>
<span data-ttu-id="2bb34-121">Specifica il nome del server in cui questo cmdlet configura il collegamento di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="2bb34-121">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="2bb34-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2bb34-122">-Confirm</span></span>
<span data-ttu-id="2bb34-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bb34-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bb34-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bb34-124">-WhatIf</span></span>
<span data-ttu-id="2bb34-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2bb34-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bb34-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2bb34-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bb34-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bb34-127">-DefaultProfile</span></span>
<span data-ttu-id="2bb34-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2bb34-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bb34-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bb34-129">CommonParameters</span></span>
<span data-ttu-id="2bb34-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bb34-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bb34-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bb34-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bb34-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2bb34-132">INPUTS</span></span>

## <span data-ttu-id="2bb34-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2bb34-133">OUTPUTS</span></span>

### <span data-ttu-id="2bb34-134">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="2bb34-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="2bb34-135">Note</span><span class="sxs-lookup"><span data-stu-id="2bb34-135">NOTES</span></span>
* <span data-ttu-id="2bb34-136">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="2bb34-136">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="2bb34-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2bb34-137">RELATED LINKS</span></span>

[<span data-ttu-id="2bb34-138">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="2bb34-138">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="2bb34-139">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="2bb34-139">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="2bb34-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="2bb34-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
