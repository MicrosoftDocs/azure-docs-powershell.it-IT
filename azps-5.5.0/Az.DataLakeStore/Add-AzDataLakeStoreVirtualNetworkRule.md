---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 8fbb586e1829cd40302ab290c2d671c67666b7e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194679"
---
# <span data-ttu-id="523d1-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="523d1-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="523d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="523d1-102">SYNOPSIS</span></span>
<span data-ttu-id="523d1-103">Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="523d1-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="523d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="523d1-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="523d1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="523d1-105">DESCRIPTION</span></span>
<span data-ttu-id="523d1-106">Il cmdlet **Add-AzDataLakeStoreVirtualNetworkRule** aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="523d1-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="523d1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="523d1-107">EXAMPLES</span></span>

### <span data-ttu-id="523d1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="523d1-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="523d1-109">Viene creata una nuova regola di rete virtuale denominata "myVNET" nell'account "dls" con un ID subnet "testId"</span><span class="sxs-lookup"><span data-stu-id="523d1-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="523d1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="523d1-110">PARAMETERS</span></span>

### <span data-ttu-id="523d1-111">-Account</span><span class="sxs-lookup"><span data-stu-id="523d1-111">-Account</span></span>
<span data-ttu-id="523d1-112">Account Data Lake Store a cui aggiungere la regola di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="523d1-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="523d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="523d1-113">-DefaultProfile</span></span>
<span data-ttu-id="523d1-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="523d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="523d1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="523d1-115">-Name</span></span>
<span data-ttu-id="523d1-116">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="523d1-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="523d1-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="523d1-117">-SubnetId</span></span>
<span data-ttu-id="523d1-118">SubnetId della regola di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="523d1-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="523d1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="523d1-119">-Confirm</span></span>
<span data-ttu-id="523d1-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="523d1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="523d1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="523d1-121">-WhatIf</span></span>
<span data-ttu-id="523d1-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="523d1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="523d1-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="523d1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="523d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="523d1-124">CommonParameters</span></span>
<span data-ttu-id="523d1-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="523d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="523d1-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="523d1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="523d1-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="523d1-127">INPUTS</span></span>

### <span data-ttu-id="523d1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="523d1-128">System.String</span></span>

## <span data-ttu-id="523d1-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="523d1-129">OUTPUTS</span></span>

### <span data-ttu-id="523d1-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="523d1-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="523d1-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="523d1-131">NOTES</span></span>

## <span data-ttu-id="523d1-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="523d1-132">RELATED LINKS</span></span>
