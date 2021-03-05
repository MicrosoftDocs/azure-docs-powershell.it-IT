---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 7a753f721e008a0c40f6a690d5c595a524ddc12b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964765"
---
# <span data-ttu-id="48180-101">Remove-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="48180-101">Remove-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="48180-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48180-102">SYNOPSIS</span></span>
<span data-ttu-id="48180-103">Rimuove la regola del firewall specificata nel Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="48180-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="48180-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48180-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48180-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="48180-105">DESCRIPTION</span></span>
<span data-ttu-id="48180-106">Il cmdlet **Remove-AzDataLakeStoreFirewallRule** rimuove la regola del firewall specificata nel Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="48180-106">The **Remove-AzDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="48180-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48180-107">EXAMPLES</span></span>

### <span data-ttu-id="48180-108">Esempio 1: Rimuovere una regola del firewall da un account</span><span class="sxs-lookup"><span data-stu-id="48180-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="48180-109">Rimuove la regola del firewall "MyFirewallRule" dall'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="48180-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="48180-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48180-110">PARAMETERS</span></span>

### <span data-ttu-id="48180-111">-Account</span><span class="sxs-lookup"><span data-stu-id="48180-111">-Account</span></span>
<span data-ttu-id="48180-112">Account Data Lake Store in cui aggiornare la regola del firewall in</span><span class="sxs-lookup"><span data-stu-id="48180-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="48180-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48180-113">-DefaultProfile</span></span>
<span data-ttu-id="48180-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="48180-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48180-115">-Name</span><span class="sxs-lookup"><span data-stu-id="48180-115">-Name</span></span>
<span data-ttu-id="48180-116">Nome della regola del firewall da eliminare.</span><span class="sxs-lookup"><span data-stu-id="48180-116">The name of the firewall rule to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48180-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48180-117">-PassThru</span></span>
<span data-ttu-id="48180-118">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="48180-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48180-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48180-119">-ResourceGroupName</span></span>
<span data-ttu-id="48180-120">Specifica il nome del gruppo di risorse che contiene l'account da cui rimuovere la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="48180-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48180-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48180-121">-Confirm</span></span>
<span data-ttu-id="48180-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48180-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48180-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48180-123">-WhatIf</span></span>
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

### <span data-ttu-id="48180-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48180-124">CommonParameters</span></span>
<span data-ttu-id="48180-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48180-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48180-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48180-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48180-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="48180-127">INPUTS</span></span>

### <span data-ttu-id="48180-128">System.String</span><span class="sxs-lookup"><span data-stu-id="48180-128">System.String</span></span>

### <span data-ttu-id="48180-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="48180-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="48180-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48180-130">OUTPUTS</span></span>

### <span data-ttu-id="48180-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="48180-131">System.Boolean</span></span>

## <span data-ttu-id="48180-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="48180-132">NOTES</span></span>

## <span data-ttu-id="48180-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48180-133">RELATED LINKS</span></span>
