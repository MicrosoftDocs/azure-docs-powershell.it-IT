---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 185cff3d51f100c922f0a23acf1d96428fb52760
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688215"
---
# <span data-ttu-id="f60ce-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f60ce-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="f60ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f60ce-102">SYNOPSIS</span></span>
<span data-ttu-id="f60ce-103">Rimuove una configurazione di ripristino di sistema di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f60ce-103">Removes a SQL database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f60ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f60ce-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f60ce-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f60ce-105">DESCRIPTION</span></span>
<span data-ttu-id="f60ce-106">Il cmdlet **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** rimuove una configurazione di ripristino di sistema di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f60ce-106">The **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="f60ce-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f60ce-107">EXAMPLES</span></span>

## <span data-ttu-id="f60ce-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f60ce-108">PARAMETERS</span></span>

### <span data-ttu-id="f60ce-109">-Force</span><span class="sxs-lookup"><span data-stu-id="f60ce-109">-Force</span></span>
<span data-ttu-id="f60ce-110">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f60ce-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f60ce-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f60ce-111">-ResourceGroupName</span></span>
<span data-ttu-id="f60ce-112">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f60ce-112">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f60ce-113">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="f60ce-113">-ServerName</span></span>
<span data-ttu-id="f60ce-114">Specifica il nome di un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="f60ce-114">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="f60ce-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="f60ce-115">-VirtualEndpointName</span></span>
<span data-ttu-id="f60ce-116">Specifica il nome di un punto finale virtuale.</span><span class="sxs-lookup"><span data-stu-id="f60ce-116">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="f60ce-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f60ce-117">-Confirm</span></span>
<span data-ttu-id="f60ce-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f60ce-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f60ce-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f60ce-119">-WhatIf</span></span>
<span data-ttu-id="f60ce-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f60ce-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f60ce-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f60ce-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f60ce-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f60ce-122">-DefaultProfile</span></span>
<span data-ttu-id="f60ce-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f60ce-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f60ce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f60ce-124">CommonParameters</span></span>
<span data-ttu-id="f60ce-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f60ce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f60ce-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f60ce-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f60ce-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f60ce-127">INPUTS</span></span>

## <span data-ttu-id="f60ce-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f60ce-128">OUTPUTS</span></span>

## <span data-ttu-id="f60ce-129">Note</span><span class="sxs-lookup"><span data-stu-id="f60ce-129">NOTES</span></span>

## <span data-ttu-id="f60ce-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f60ce-130">RELATED LINKS</span></span>

[<span data-ttu-id="f60ce-131">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f60ce-131">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f60ce-132">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f60ce-132">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f60ce-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f60ce-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f60ce-134">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="f60ce-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
