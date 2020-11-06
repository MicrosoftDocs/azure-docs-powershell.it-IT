---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
ms.openlocfilehash: 472e8e7a2f0919115686764136b6b40f5e1da913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514083"
---
# <span data-ttu-id="67337-101">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="67337-101">Get-AzureRmSqlDatabaseExpanded</span></span>

## <span data-ttu-id="67337-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67337-102">SYNOPSIS</span></span>
<span data-ttu-id="67337-103">Ottiene un database e i relativi valori di proprietà espanse.</span><span class="sxs-lookup"><span data-stu-id="67337-103">Gets a database and its expanded property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67337-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67337-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67337-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67337-105">DESCRIPTION</span></span>
<span data-ttu-id="67337-106">Il cmdlet **Get-AzureRmSqlDatabaseExpanded** ottiene un database e i relativi valori di proprietà espansi.</span><span class="sxs-lookup"><span data-stu-id="67337-106">The **Get-AzureRmSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>

<span data-ttu-id="67337-107">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="67337-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="67337-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67337-108">EXAMPLES</span></span>

### <span data-ttu-id="67337-109">Esempio 1: ottenere un oggetto di database con informazioni su Service Tier Advisor</span><span class="sxs-lookup"><span data-stu-id="67337-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\>Get-AzureSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="67337-110">Questo comando restituisce il database con proprietà espanse che contengono le informazioni di Advisor del livello di servizio.</span><span class="sxs-lookup"><span data-stu-id="67337-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

## <span data-ttu-id="67337-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67337-111">PARAMETERS</span></span>

### <span data-ttu-id="67337-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="67337-112">-DatabaseName</span></span>
<span data-ttu-id="67337-113">Specifica il nome del database da ottenere.</span><span class="sxs-lookup"><span data-stu-id="67337-113">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="67337-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67337-114">-DefaultProfile</span></span>
<span data-ttu-id="67337-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="67337-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67337-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67337-116">-ResourceGroupName</span></span>
<span data-ttu-id="67337-117">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="67337-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="67337-118">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="67337-118">-ServerName</span></span>
<span data-ttu-id="67337-119">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="67337-119">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="67337-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="67337-120">-Confirm</span></span>
<span data-ttu-id="67337-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67337-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67337-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67337-122">-WhatIf</span></span>
<span data-ttu-id="67337-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67337-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67337-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67337-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67337-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67337-125">CommonParameters</span></span>
<span data-ttu-id="67337-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67337-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67337-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67337-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67337-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67337-128">INPUTS</span></span>

### <span data-ttu-id="67337-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="67337-129">None</span></span>
<span data-ttu-id="67337-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="67337-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67337-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67337-131">OUTPUTS</span></span>

## <span data-ttu-id="67337-132">Note</span><span class="sxs-lookup"><span data-stu-id="67337-132">NOTES</span></span>

## <span data-ttu-id="67337-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67337-133">RELATED LINKS</span></span>

[<span data-ttu-id="67337-134">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="67337-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
