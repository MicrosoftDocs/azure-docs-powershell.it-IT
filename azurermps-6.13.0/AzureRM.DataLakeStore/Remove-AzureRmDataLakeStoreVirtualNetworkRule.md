---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 196d0eba5119ab984f9ffc632a301d3e65157f63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686418"
---
# <span data-ttu-id="04ec1-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="04ec1-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="04ec1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="04ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="04ec1-103">Rimuove la regola di rete virtuale specificata nello Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="04ec1-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04ec1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04ec1-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04ec1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04ec1-105">DESCRIPTION</span></span>
<span data-ttu-id="04ec1-106">Il cmdlet **Remove-AzureRmDataLakeStoreVirtualNetworkRule** rimuove la regola di rete virtuale specificata nello Store Data Lake di dati specificato.</span><span class="sxs-lookup"><span data-stu-id="04ec1-106">The **Remove-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="04ec1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04ec1-107">EXAMPLES</span></span>

### <span data-ttu-id="04ec1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="04ec1-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="04ec1-109">Rimuove la regola di rete virtuale "myVNET" dall'account "DLS"</span><span class="sxs-lookup"><span data-stu-id="04ec1-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="04ec1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04ec1-110">PARAMETERS</span></span>

### <span data-ttu-id="04ec1-111">-Account</span><span class="sxs-lookup"><span data-stu-id="04ec1-111">-Account</span></span>
<span data-ttu-id="04ec1-112">L'account di data Lake Store per aggiornare la regola della rete virtuale in</span><span class="sxs-lookup"><span data-stu-id="04ec1-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="04ec1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ec1-113">-DefaultProfile</span></span>
<span data-ttu-id="04ec1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="04ec1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04ec1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="04ec1-115">-Name</span></span>
<span data-ttu-id="04ec1-116">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="04ec1-116">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ec1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04ec1-117">-PassThru</span></span>
<span data-ttu-id="04ec1-118">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="04ec1-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="04ec1-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="04ec1-119">-Confirm</span></span>
<span data-ttu-id="04ec1-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04ec1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04ec1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04ec1-121">-WhatIf</span></span>
<span data-ttu-id="04ec1-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04ec1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04ec1-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04ec1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04ec1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ec1-124">CommonParameters</span></span>
<span data-ttu-id="04ec1-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04ec1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ec1-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04ec1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ec1-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="04ec1-127">INPUTS</span></span>

### <span data-ttu-id="04ec1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="04ec1-128">System.String</span></span>

### <span data-ttu-id="04ec1-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="04ec1-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="04ec1-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04ec1-130">OUTPUTS</span></span>

### <span data-ttu-id="04ec1-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04ec1-131">System.Boolean</span></span>

## <span data-ttu-id="04ec1-132">Note</span><span class="sxs-lookup"><span data-stu-id="04ec1-132">NOTES</span></span>

## <span data-ttu-id="04ec1-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04ec1-133">RELATED LINKS</span></span>
