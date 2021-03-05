---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 580b5518e1fc0894a51920e781464258bef9e9cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966669"
---
# <span data-ttu-id="1aae4-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1aae4-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="1aae4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aae4-102">SYNOPSIS</span></span>
<span data-ttu-id="1aae4-103">Ottiene le regole del firewall specificate nel Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="1aae4-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="1aae4-104">Se non viene specificata alcuna regola del firewall, vengono elencate tutte le regole del firewall per l'account.</span><span class="sxs-lookup"><span data-stu-id="1aae4-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="1aae4-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1aae4-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1aae4-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1aae4-106">DESCRIPTION</span></span>
<span data-ttu-id="1aae4-107">Il Get-AzDataLakeStoreFirewallRule cmdlet recupera le regole del firewall specificate nel Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="1aae4-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="1aae4-108">Se non viene specificata alcuna regola del firewall, vengono elencate tutte le regole del firewall per l'account.</span><span class="sxs-lookup"><span data-stu-id="1aae4-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="1aae4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1aae4-109">EXAMPLES</span></span>

### <span data-ttu-id="1aae4-110">Esempio 1: Recuperare una regola del firewall specifica</span><span class="sxs-lookup"><span data-stu-id="1aae4-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="1aae4-111">Restituisce la regola del firewall denominata "MyFirewallRule" dall'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="1aae4-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="1aae4-112">Esempio 2: Elencare tutte le regole del firewall in un account</span><span class="sxs-lookup"><span data-stu-id="1aae4-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="1aae4-113">Restituisce tutte le regole del firewall nell'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="1aae4-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="1aae4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1aae4-114">PARAMETERS</span></span>

### <span data-ttu-id="1aae4-115">-Account</span><span class="sxs-lookup"><span data-stu-id="1aae4-115">-Account</span></span>
<span data-ttu-id="1aae4-116">Account Data Lake Store da cui recuperare la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="1aae4-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="1aae4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aae4-117">-DefaultProfile</span></span>
<span data-ttu-id="1aae4-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1aae4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1aae4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1aae4-119">-Name</span></span>
<span data-ttu-id="1aae4-120">Nome della regola del firewall da recuperare</span><span class="sxs-lookup"><span data-stu-id="1aae4-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="1aae4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aae4-121">-ResourceGroupName</span></span>
<span data-ttu-id="1aae4-122">Nome del gruppo di risorse in cui si vuole recuperare la regola del firewall specificata dall'account specificato.</span><span class="sxs-lookup"><span data-stu-id="1aae4-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aae4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aae4-123">CommonParameters</span></span>
<span data-ttu-id="1aae4-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aae4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aae4-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aae4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aae4-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="1aae4-126">INPUTS</span></span>

### <span data-ttu-id="1aae4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="1aae4-127">System.String</span></span>

## <span data-ttu-id="1aae4-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1aae4-128">OUTPUTS</span></span>

### <span data-ttu-id="1aae4-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1aae4-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="1aae4-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="1aae4-130">NOTES</span></span>

## <span data-ttu-id="1aae4-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1aae4-131">RELATED LINKS</span></span>
