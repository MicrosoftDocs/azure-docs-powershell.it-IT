---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 3b5a512e5c301e328bf556d63d7ecb9191a08c5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688056"
---
# <span data-ttu-id="b2225-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2225-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="b2225-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2225-102">SYNOPSIS</span></span>
<span data-ttu-id="b2225-103">Rimuove una configurazione di ripristino di sistema di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b2225-103">Removes a SQL database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2225-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2225-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2225-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2225-105">DESCRIPTION</span></span>
<span data-ttu-id="b2225-106">Il cmdlet **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** rimuove una configurazione di ripristino di sistema di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b2225-106">The **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="b2225-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2225-107">EXAMPLES</span></span>

## <span data-ttu-id="b2225-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2225-108">PARAMETERS</span></span>

### <span data-ttu-id="b2225-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2225-109">-DefaultProfile</span></span>
<span data-ttu-id="b2225-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b2225-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2225-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b2225-111">-Force</span></span>
<span data-ttu-id="b2225-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b2225-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b2225-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2225-113">-ResourceGroupName</span></span>
<span data-ttu-id="b2225-114">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2225-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b2225-115">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b2225-115">-ServerName</span></span>
<span data-ttu-id="b2225-116">Specifica il nome di un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="b2225-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="b2225-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="b2225-117">-VirtualEndpointName</span></span>
<span data-ttu-id="b2225-118">Specifica il nome di un punto finale virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2225-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2225-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b2225-119">-Confirm</span></span>
<span data-ttu-id="b2225-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2225-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2225-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2225-121">-WhatIf</span></span>
<span data-ttu-id="b2225-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2225-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2225-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2225-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2225-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2225-124">CommonParameters</span></span>
<span data-ttu-id="b2225-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2225-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2225-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2225-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2225-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2225-127">INPUTS</span></span>

### <span data-ttu-id="b2225-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b2225-128">System.String</span></span>

## <span data-ttu-id="b2225-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2225-129">OUTPUTS</span></span>

### <span data-ttu-id="b2225-130">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="b2225-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="b2225-131">Note</span><span class="sxs-lookup"><span data-stu-id="b2225-131">NOTES</span></span>

## <span data-ttu-id="b2225-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2225-132">RELATED LINKS</span></span>

[<span data-ttu-id="b2225-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2225-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b2225-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2225-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b2225-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2225-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="b2225-136">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="b2225-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)