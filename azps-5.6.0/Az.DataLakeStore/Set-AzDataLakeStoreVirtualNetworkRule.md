---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 98f4dd2a1076df1954674f67829e3ee14da1d871
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995580"
---
# <span data-ttu-id="1cc80-101">Set-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1cc80-101">Set-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="1cc80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cc80-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc80-103">Modifica la regola di rete virtuale specificata nell'archivio dati specificato.</span><span class="sxs-lookup"><span data-stu-id="1cc80-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="1cc80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1cc80-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cc80-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1cc80-105">DESCRIPTION</span></span>
<span data-ttu-id="1cc80-106">Il cmdlet **Set-AzDataLakeStoreVirtualNetworkRule** modifica la regola di rete virtuale specificata nel data lake store specificato.</span><span class="sxs-lookup"><span data-stu-id="1cc80-106">The **Set-AzDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="1cc80-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1cc80-107">EXAMPLES</span></span>

### <span data-ttu-id="1cc80-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1cc80-108">Example 1</span></span>
```powershell
PS C:\> Set-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="1cc80-109">Aggiorna l'ID subnet della regola di rete virtuale "myVNET" nell'account "dls" in "updatedId"</span><span class="sxs-lookup"><span data-stu-id="1cc80-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="1cc80-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cc80-110">PARAMETERS</span></span>

### <span data-ttu-id="1cc80-111">-Account</span><span class="sxs-lookup"><span data-stu-id="1cc80-111">-Account</span></span>
<span data-ttu-id="1cc80-112">Account Data Lake Store in cui aggiornare la regola di rete virtuale in</span><span class="sxs-lookup"><span data-stu-id="1cc80-112">The Data Lake Store account to update the virtual network rule in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cc80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc80-113">-DefaultProfile</span></span>
<span data-ttu-id="1cc80-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc80-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cc80-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1cc80-115">-Name</span></span>
<span data-ttu-id="1cc80-116">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1cc80-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="1cc80-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1cc80-117">-SubnetId</span></span>
<span data-ttu-id="1cc80-118">Inizio dell'intervallo IP valido per la regola di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="1cc80-118">The start of the valid ip range for the virtual network rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cc80-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cc80-119">-Confirm</span></span>
<span data-ttu-id="1cc80-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cc80-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cc80-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cc80-121">-WhatIf</span></span>
<span data-ttu-id="1cc80-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1cc80-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cc80-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1cc80-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cc80-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc80-124">CommonParameters</span></span>
<span data-ttu-id="1cc80-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cc80-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc80-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cc80-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc80-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="1cc80-127">INPUTS</span></span>

### <span data-ttu-id="1cc80-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1cc80-128">System.String</span></span>

## <span data-ttu-id="1cc80-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1cc80-129">OUTPUTS</span></span>

### <span data-ttu-id="1cc80-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1cc80-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="1cc80-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="1cc80-131">NOTES</span></span>

## <span data-ttu-id="1cc80-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1cc80-132">RELATED LINKS</span></span>
