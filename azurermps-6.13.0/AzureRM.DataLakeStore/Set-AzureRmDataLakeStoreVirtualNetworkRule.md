---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: b05158ae21219760c9c88fe9c0ae3e4978b76f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513888"
---
# <span data-ttu-id="49450-101">Set-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="49450-101">Set-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="49450-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49450-102">SYNOPSIS</span></span>
<span data-ttu-id="49450-103">Modifica la regola di rete virtuale specificata nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="49450-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49450-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49450-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49450-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49450-105">DESCRIPTION</span></span>
<span data-ttu-id="49450-106">Il cmdlet **set-AzureRmDataLakeStoreVirtualNetworkRule** modifica la regola di rete virtuale specificata nello Store Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="49450-106">The **Set-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="49450-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49450-107">EXAMPLES</span></span>

### <span data-ttu-id="49450-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="49450-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="49450-109">Aggiorna l'ID subnet della regola di rete virtuale "myVNET" nell'account "DLS" in "updatedId"</span><span class="sxs-lookup"><span data-stu-id="49450-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="49450-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49450-110">PARAMETERS</span></span>

### <span data-ttu-id="49450-111">-Account</span><span class="sxs-lookup"><span data-stu-id="49450-111">-Account</span></span>
<span data-ttu-id="49450-112">L'account di data Lake Store per aggiornare la regola della rete virtuale in</span><span class="sxs-lookup"><span data-stu-id="49450-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="49450-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49450-113">-DefaultProfile</span></span>
<span data-ttu-id="49450-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49450-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49450-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="49450-115">-Name</span></span>
<span data-ttu-id="49450-116">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="49450-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="49450-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="49450-117">-SubnetId</span></span>
<span data-ttu-id="49450-118">Inizio dell'intervallo IP valido per la regola di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="49450-118">The start of the valid ip range for the virtual network rule</span></span>

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

### <span data-ttu-id="49450-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="49450-119">-Confirm</span></span>
<span data-ttu-id="49450-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49450-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49450-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49450-121">-WhatIf</span></span>
<span data-ttu-id="49450-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49450-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49450-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49450-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49450-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49450-124">CommonParameters</span></span>
<span data-ttu-id="49450-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49450-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49450-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49450-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49450-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49450-127">INPUTS</span></span>

### <span data-ttu-id="49450-128">System. String</span><span class="sxs-lookup"><span data-stu-id="49450-128">System.String</span></span>

## <span data-ttu-id="49450-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49450-129">OUTPUTS</span></span>

### <span data-ttu-id="49450-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="49450-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="49450-131">Note</span><span class="sxs-lookup"><span data-stu-id="49450-131">NOTES</span></span>

## <span data-ttu-id="49450-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49450-132">RELATED LINKS</span></span>
