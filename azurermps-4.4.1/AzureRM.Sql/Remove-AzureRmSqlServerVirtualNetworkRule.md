---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8c680cf87deedf5fc4bd8671a60db4329a1f68ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688504"
---
# <span data-ttu-id="abc5a-101">Remove-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="abc5a-101">Remove-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="abc5a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="abc5a-102">SYNOPSIS</span></span>
<span data-ttu-id="abc5a-103">Elimina una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="abc5a-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abc5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="abc5a-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abc5a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abc5a-105">DESCRIPTION</span></span>
<span data-ttu-id="abc5a-106">Questo comando Elimina una regola di rete virtuale di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="abc5a-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="abc5a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="abc5a-107">EXAMPLES</span></span>

### <span data-ttu-id="abc5a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="abc5a-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="abc5a-109">Elimina una regola di rete virtuale di Azure SQL Server esistente</span><span class="sxs-lookup"><span data-stu-id="abc5a-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="abc5a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="abc5a-110">PARAMETERS</span></span>

### <span data-ttu-id="abc5a-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abc5a-111">-ResourceGroupName</span></span>
<span data-ttu-id="abc5a-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="abc5a-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="abc5a-113">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="abc5a-113">-ServerName</span></span>
<span data-ttu-id="abc5a-114">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="abc5a-114">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="abc5a-115">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="abc5a-115">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="abc5a-116">Nome della regola di rete virtuale di Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="abc5a-116">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="abc5a-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="abc5a-117">-Confirm</span></span>
<span data-ttu-id="abc5a-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abc5a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abc5a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abc5a-119">-WhatIf</span></span>
<span data-ttu-id="abc5a-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="abc5a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abc5a-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="abc5a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abc5a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc5a-122">-DefaultProfile</span></span>
<span data-ttu-id="abc5a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="abc5a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abc5a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc5a-124">CommonParameters</span></span>
<span data-ttu-id="abc5a-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abc5a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc5a-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abc5a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc5a-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="abc5a-127">INPUTS</span></span>

### <span data-ttu-id="abc5a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="abc5a-128">System.String</span></span>

## <span data-ttu-id="abc5a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="abc5a-129">OUTPUTS</span></span>

### <span data-ttu-id="abc5a-130">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="abc5a-130">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="abc5a-131">Note</span><span class="sxs-lookup"><span data-stu-id="abc5a-131">NOTES</span></span>

## <span data-ttu-id="abc5a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="abc5a-132">RELATED LINKS</span></span>

