---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 483b71d53dfb4754a4fa5f00331b07a685102782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512228"
---
# <span data-ttu-id="06b15-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="06b15-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="06b15-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06b15-102">SYNOPSIS</span></span>
<span data-ttu-id="06b15-103">Ottiene una configurazione di ripristino di sistema del server di database.</span><span class="sxs-lookup"><span data-stu-id="06b15-103">Gets a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06b15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06b15-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06b15-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06b15-105">DESCRIPTION</span></span>
<span data-ttu-id="06b15-106">Il cmdlet **Get-AzureRmSqlServerDisasterRecoveryConfiguration** ottiene una configurazione di ripristino del sistema di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="06b15-106">The **Get-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="06b15-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06b15-107">EXAMPLES</span></span>

## <span data-ttu-id="06b15-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06b15-108">PARAMETERS</span></span>

### <span data-ttu-id="06b15-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b15-109">-DefaultProfile</span></span>
<span data-ttu-id="06b15-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="06b15-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06b15-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06b15-111">-ResourceGroupName</span></span>
<span data-ttu-id="06b15-112">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="06b15-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="06b15-113">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="06b15-113">-ServerName</span></span>
<span data-ttu-id="06b15-114">Specifica il nome del server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="06b15-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="06b15-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="06b15-115">-VirtualEndpointName</span></span>
<span data-ttu-id="06b15-116">Specifica il nome del punto finale virtuale.</span><span class="sxs-lookup"><span data-stu-id="06b15-116">Specifies the name of the virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b15-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="06b15-117">-Confirm</span></span>
<span data-ttu-id="06b15-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06b15-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06b15-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06b15-119">-WhatIf</span></span>
<span data-ttu-id="06b15-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06b15-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06b15-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06b15-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06b15-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b15-122">CommonParameters</span></span>
<span data-ttu-id="06b15-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06b15-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b15-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06b15-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b15-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06b15-125">INPUTS</span></span>

### <span data-ttu-id="06b15-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="06b15-126">None</span></span>
<span data-ttu-id="06b15-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="06b15-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06b15-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06b15-128">OUTPUTS</span></span>

## <span data-ttu-id="06b15-129">Note</span><span class="sxs-lookup"><span data-stu-id="06b15-129">NOTES</span></span>

## <span data-ttu-id="06b15-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06b15-130">RELATED LINKS</span></span>

[<span data-ttu-id="06b15-131">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="06b15-131">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="06b15-132">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="06b15-132">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="06b15-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="06b15-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="06b15-134">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="06b15-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

