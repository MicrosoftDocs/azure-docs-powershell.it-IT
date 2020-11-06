---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 972F4188-52C5-4B92-8B88-E68526537F48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 1b8e99b195866ac63f649d4484a0cfb631b09e10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507839"
---
# <span data-ttu-id="c5f76-101">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="c5f76-101">Stop-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="c5f76-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5f76-102">SYNOPSIS</span></span>
<span data-ttu-id="c5f76-103">Interrompe l'aggiornamento di un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="c5f76-103">Stops the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5f76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5f76-104">SYNTAX</span></span>

```
Stop-AzureRmSqlServerUpgrade [-Force] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5f76-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5f76-105">DESCRIPTION</span></span>
<span data-ttu-id="c5f76-106">Il cmdlet **Stop-AzureRmSqlServerUpgrade** interrompe l'aggiornamento di un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="c5f76-106">The **Stop-AzureRmSqlServerUpgrade** cmdlet stops the upgrade of an Azure SQL Database server.</span></span>

## <span data-ttu-id="c5f76-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5f76-107">EXAMPLES</span></span>

### <span data-ttu-id="c5f76-108">Esempio 1: arrestare un aggiornamento del server</span><span class="sxs-lookup"><span data-stu-id="c5f76-108">Example 1: Stop a server upgrade</span></span>
```
PS C:\>Stop-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server02"
```

<span data-ttu-id="c5f76-109">Questo comando interrompe la richiesta di aggiornamento del server denominato Server02 assegnato al gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="c5f76-109">This command stops the request to upgrade the server named Server02 assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="c5f76-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5f76-110">PARAMETERS</span></span>

### <span data-ttu-id="c5f76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5f76-111">-DefaultProfile</span></span>
<span data-ttu-id="c5f76-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c5f76-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5f76-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c5f76-113">-Force</span></span>
<span data-ttu-id="c5f76-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c5f76-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5f76-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5f76-115">-ResourceGroupName</span></span>
<span data-ttu-id="c5f76-116">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="c5f76-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c5f76-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="c5f76-117">-ServerName</span></span>
<span data-ttu-id="c5f76-118">Specifica il nome del server per cui questo cmdlet arresta un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c5f76-118">Specifies the name of the server for which this cmdlet stops an upgrade.</span></span>

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

### <span data-ttu-id="c5f76-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c5f76-119">-Confirm</span></span>
<span data-ttu-id="c5f76-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5f76-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5f76-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5f76-121">-WhatIf</span></span>
<span data-ttu-id="c5f76-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5f76-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5f76-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5f76-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5f76-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5f76-124">CommonParameters</span></span>
<span data-ttu-id="c5f76-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5f76-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5f76-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5f76-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5f76-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5f76-127">INPUTS</span></span>

### <span data-ttu-id="c5f76-128">Microsoft. Azure. Commands. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="c5f76-128">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="c5f76-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5f76-129">OUTPUTS</span></span>

## <span data-ttu-id="c5f76-130">Note</span><span class="sxs-lookup"><span data-stu-id="c5f76-130">NOTES</span></span>

## <span data-ttu-id="c5f76-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5f76-131">RELATED LINKS</span></span>

[<span data-ttu-id="c5f76-132">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="c5f76-132">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="c5f76-133">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="c5f76-133">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="c5f76-134">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="c5f76-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


