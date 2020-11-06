---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B3776B0B-FBC8-407A-A8A4-583C346CCF12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 7f48385c7002f353ca34f399d40310a9e0469977
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509044"
---
# <span data-ttu-id="4f787-101">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="4f787-101">Get-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="4f787-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f787-102">SYNOPSIS</span></span>
<span data-ttu-id="4f787-103">Ottiene lo stato di un aggiornamento del server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f787-103">Gets the status of an Azure SQL Database server upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f787-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f787-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgrade -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f787-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f787-105">DESCRIPTION</span></span>
<span data-ttu-id="4f787-106">Il cmdlet **Get-AzureRmSqlServerUpgrade** ottiene lo stato di un aggiornamento del server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f787-106">The **Get-AzureRmSqlServerUpgrade** cmdlet gets the status of an Azure SQL Database server upgrade.</span></span>

## <span data-ttu-id="4f787-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f787-107">EXAMPLES</span></span>

### <span data-ttu-id="4f787-108">Esempio 1: ottenere lo stato di un aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4f787-108">Example 1: Get the status of an upgrade</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceGroupName               : resourcegroup01
ServerName                      : server01
Status                          : Queued
```

<span data-ttu-id="4f787-109">Questo comando ottiene lo stato di un aggiornamento dal server denominato Server01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="4f787-109">This command gets the status of an upgrade from the server named Server01 in resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="4f787-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f787-110">PARAMETERS</span></span>

### <span data-ttu-id="4f787-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f787-111">-DefaultProfile</span></span>
<span data-ttu-id="4f787-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4f787-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f787-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f787-113">-ResourceGroupName</span></span>
<span data-ttu-id="4f787-114">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="4f787-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="4f787-115">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4f787-115">-ServerName</span></span>
<span data-ttu-id="4f787-116">Specifica il nome del server per cui questo cmdlet ottiene lo stato di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4f787-116">Specifies the name of the server for which this cmdlet gets upgrade status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f787-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4f787-117">-Confirm</span></span>
<span data-ttu-id="4f787-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f787-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f787-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f787-119">-WhatIf</span></span>
<span data-ttu-id="4f787-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f787-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f787-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f787-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f787-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f787-122">CommonParameters</span></span>
<span data-ttu-id="4f787-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f787-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f787-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f787-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f787-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f787-125">INPUTS</span></span>

### <span data-ttu-id="4f787-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4f787-126">System.String</span></span>

## <span data-ttu-id="4f787-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f787-127">OUTPUTS</span></span>

### <span data-ttu-id="4f787-128">Microsoft. Azure. Commands. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="4f787-128">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="4f787-129">Note</span><span class="sxs-lookup"><span data-stu-id="4f787-129">NOTES</span></span>

## <span data-ttu-id="4f787-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f787-130">RELATED LINKS</span></span>

[<span data-ttu-id="4f787-131">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="4f787-131">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="4f787-132">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="4f787-132">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="4f787-133">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="4f787-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


