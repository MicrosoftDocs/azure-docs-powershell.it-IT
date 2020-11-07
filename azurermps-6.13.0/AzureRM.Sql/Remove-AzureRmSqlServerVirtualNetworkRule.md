---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: c6011b1b8b23c5fd6a21075199f6a6d89c72e0cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687563"
---
# <span data-ttu-id="f2777-101">Remove-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f2777-101">Remove-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="f2777-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2777-102">SYNOPSIS</span></span>
<span data-ttu-id="f2777-103">Elimina una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f2777-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2777-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2777-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2777-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2777-105">DESCRIPTION</span></span>
<span data-ttu-id="f2777-106">Questo comando Elimina una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f2777-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="f2777-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2777-107">EXAMPLES</span></span>

### <span data-ttu-id="f2777-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f2777-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="f2777-109">Elimina una regola di rete virtuale di Azure SQL Server esistente</span><span class="sxs-lookup"><span data-stu-id="f2777-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="f2777-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2777-110">PARAMETERS</span></span>

### <span data-ttu-id="f2777-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2777-111">-AsJob</span></span>
<span data-ttu-id="f2777-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f2777-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2777-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2777-113">-DefaultProfile</span></span>
<span data-ttu-id="f2777-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f2777-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2777-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2777-115">-ResourceGroupName</span></span>
<span data-ttu-id="f2777-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f2777-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="f2777-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="f2777-117">-ServerName</span></span>
<span data-ttu-id="f2777-118">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f2777-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="f2777-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="f2777-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="f2777-120">Nome della regola di rete virtuale di Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="f2777-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="f2777-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f2777-121">-Confirm</span></span>
<span data-ttu-id="f2777-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2777-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2777-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2777-123">-WhatIf</span></span>
<span data-ttu-id="f2777-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2777-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2777-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2777-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2777-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2777-126">CommonParameters</span></span>
<span data-ttu-id="f2777-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2777-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2777-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2777-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2777-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2777-129">INPUTS</span></span>

### <span data-ttu-id="f2777-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f2777-130">System.String</span></span>

## <span data-ttu-id="f2777-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2777-131">OUTPUTS</span></span>

### <span data-ttu-id="f2777-132">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="f2777-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="f2777-133">Note</span><span class="sxs-lookup"><span data-stu-id="f2777-133">NOTES</span></span>

## <span data-ttu-id="f2777-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2777-134">RELATED LINKS</span></span>
