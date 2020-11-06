---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 08d14217cff370557009167e09cd7e5396df4e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510243"
---
# <span data-ttu-id="80e14-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="80e14-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="80e14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80e14-102">SYNOPSIS</span></span>
<span data-ttu-id="80e14-103">Crea una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="80e14-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80e14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80e14-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80e14-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80e14-105">DESCRIPTION</span></span>
<span data-ttu-id="80e14-106">Crea una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="80e14-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="80e14-107">Le regole di rete virtuale vengono usate per connettere Azure SQL Server a una rete virtuale specifica per limitare l'accesso a Azure SQL Server solo per essere disponibile all'interno della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="80e14-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="80e14-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80e14-108">EXAMPLES</span></span>

### <span data-ttu-id="80e14-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="80e14-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="80e14-110">Crea una regola di rete virtuale di Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="80e14-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="80e14-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80e14-111">PARAMETERS</span></span>

### <span data-ttu-id="80e14-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80e14-112">-ResourceGroupName</span></span>
<span data-ttu-id="80e14-113">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="80e14-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="80e14-114">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="80e14-114">-ServerName</span></span>
<span data-ttu-id="80e14-115">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="80e14-115">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="80e14-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="80e14-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="80e14-117">Nome della regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="80e14-117">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="80e14-118">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="80e14-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="80e14-119">ID subnet della rete virtuale che specifica i dettagli di Microsoft. Network</span><span class="sxs-lookup"><span data-stu-id="80e14-119">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="80e14-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="80e14-120">-Confirm</span></span>
<span data-ttu-id="80e14-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80e14-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e14-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80e14-122">-WhatIf</span></span>
<span data-ttu-id="80e14-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80e14-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80e14-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80e14-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80e14-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80e14-125">-DefaultProfile</span></span>
<span data-ttu-id="80e14-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80e14-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80e14-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80e14-127">CommonParameters</span></span>
<span data-ttu-id="80e14-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80e14-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80e14-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80e14-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80e14-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80e14-130">INPUTS</span></span>

### <span data-ttu-id="80e14-131">System. String</span><span class="sxs-lookup"><span data-stu-id="80e14-131">System.String</span></span>

## <span data-ttu-id="80e14-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80e14-132">OUTPUTS</span></span>

### <span data-ttu-id="80e14-133">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="80e14-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="80e14-134">Note</span><span class="sxs-lookup"><span data-stu-id="80e14-134">NOTES</span></span>

## <span data-ttu-id="80e14-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80e14-135">RELATED LINKS</span></span>

