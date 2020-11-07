---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 355b8fdffd5d1e9e16fe9bfaf504d627a8b9b167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688490"
---
# <span data-ttu-id="81238-101">Set-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="81238-101">Set-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="81238-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81238-102">SYNOPSIS</span></span>
<span data-ttu-id="81238-103">Modifica la configurazione di una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="81238-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81238-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81238-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81238-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81238-105">DESCRIPTION</span></span>
<span data-ttu-id="81238-106">Questo comando consente di modificare la configurazione di una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="81238-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>


<span data-ttu-id="81238-107">Per controllare il set di regole di rete virtuale nel server, USA invece ' Add-AzureRmSqlServerVirtualNetworkRule ' è Remove-AzureRmSqlServerVirtualNetworkRule '.</span><span class="sxs-lookup"><span data-stu-id="81238-107">To control the set of virtual network rules in the server, use 'Add-AzureRmSqlServerVirtualNetworkRule' and 'Remove-AzureRmSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="81238-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81238-108">EXAMPLES</span></span>

### <span data-ttu-id="81238-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="81238-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="81238-110">Modifica una regola di rete virtuale esistente con l'ID subnet della nuova rete virtuale che contiene informazioni sulla nuova rete virtuale</span><span class="sxs-lookup"><span data-stu-id="81238-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="81238-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81238-111">PARAMETERS</span></span>

### <span data-ttu-id="81238-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81238-112">-ResourceGroupName</span></span>
<span data-ttu-id="81238-113">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="81238-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="81238-114">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="81238-114">-ServerName</span></span>
<span data-ttu-id="81238-115">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="81238-115">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="81238-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="81238-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="81238-117">Nome della regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="81238-117">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="81238-118">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="81238-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="81238-119">ID subnet di rete virtuale per la regola.</span><span class="sxs-lookup"><span data-stu-id="81238-119">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="81238-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="81238-120">-Confirm</span></span>
<span data-ttu-id="81238-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81238-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81238-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81238-122">-WhatIf</span></span>
<span data-ttu-id="81238-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81238-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81238-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81238-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81238-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81238-125">-DefaultProfile</span></span>
<span data-ttu-id="81238-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81238-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81238-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81238-127">CommonParameters</span></span>
<span data-ttu-id="81238-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81238-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81238-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81238-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81238-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81238-130">INPUTS</span></span>

### <span data-ttu-id="81238-131">System. String</span><span class="sxs-lookup"><span data-stu-id="81238-131">System.String</span></span>

## <span data-ttu-id="81238-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81238-132">OUTPUTS</span></span>

### <span data-ttu-id="81238-133">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="81238-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="81238-134">Note</span><span class="sxs-lookup"><span data-stu-id="81238-134">NOTES</span></span>

## <span data-ttu-id="81238-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81238-135">RELATED LINKS</span></span>

