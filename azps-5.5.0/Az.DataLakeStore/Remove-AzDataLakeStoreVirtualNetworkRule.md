---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 9e455b7160b731f20e5dad6230b2015f73ca5390
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180910"
---
# <span data-ttu-id="16302-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="16302-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="16302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16302-102">SYNOPSIS</span></span>
<span data-ttu-id="16302-103">Rimuove la regola di rete virtuale specificata nel Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="16302-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="16302-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16302-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16302-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="16302-105">DESCRIPTION</span></span>
<span data-ttu-id="16302-106">Il cmdlet **Remove-AzDataLakeStoreVirtualNetworkRule** rimuove la regola di rete virtuale specificata nel data lake store specificato.</span><span class="sxs-lookup"><span data-stu-id="16302-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="16302-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16302-107">EXAMPLES</span></span>

### <span data-ttu-id="16302-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="16302-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="16302-109">Rimuove la regola di rete virtuale "myVNET" dall'account "dls"</span><span class="sxs-lookup"><span data-stu-id="16302-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="16302-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16302-110">PARAMETERS</span></span>

### <span data-ttu-id="16302-111">-Account</span><span class="sxs-lookup"><span data-stu-id="16302-111">-Account</span></span>
<span data-ttu-id="16302-112">Account Data Lake Store in cui aggiornare la regola di rete virtuale in</span><span class="sxs-lookup"><span data-stu-id="16302-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="16302-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16302-113">-DefaultProfile</span></span>
<span data-ttu-id="16302-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16302-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16302-115">-Name</span><span class="sxs-lookup"><span data-stu-id="16302-115">-Name</span></span>
<span data-ttu-id="16302-116">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="16302-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="16302-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16302-117">-PassThru</span></span>
<span data-ttu-id="16302-118">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="16302-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="16302-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16302-119">-Confirm</span></span>
<span data-ttu-id="16302-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16302-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16302-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16302-121">-WhatIf</span></span>
<span data-ttu-id="16302-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16302-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16302-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16302-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16302-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16302-124">CommonParameters</span></span>
<span data-ttu-id="16302-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16302-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16302-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16302-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16302-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="16302-127">INPUTS</span></span>

### <span data-ttu-id="16302-128">System.String</span><span class="sxs-lookup"><span data-stu-id="16302-128">System.String</span></span>

## <span data-ttu-id="16302-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16302-129">OUTPUTS</span></span>

### <span data-ttu-id="16302-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="16302-130">System.Boolean</span></span>

## <span data-ttu-id="16302-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="16302-131">NOTES</span></span>

## <span data-ttu-id="16302-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16302-132">RELATED LINKS</span></span>
