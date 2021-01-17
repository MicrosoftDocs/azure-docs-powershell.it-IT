---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: c681ba089487868b556bd6e0ae198384a0dadd8c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473594"
---
# <span data-ttu-id="f7da9-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f7da9-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="f7da9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7da9-102">SYNOPSIS</span></span>
<span data-ttu-id="f7da9-103">Ottiene le regole del firewall specificate nello Store Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="f7da9-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="f7da9-104">Se non è specificata alcuna regola del firewall, elenca tutte le regole del firewall per l'account.</span><span class="sxs-lookup"><span data-stu-id="f7da9-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="f7da9-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7da9-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7da9-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7da9-106">DESCRIPTION</span></span>
<span data-ttu-id="f7da9-107">Il cmdlet Get-AzDataLakeStoreFirewallRule ottiene le regole del firewall specificate nello Store Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="f7da9-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="f7da9-108">Se non è specificata alcuna regola del firewall, elenca tutte le regole del firewall per l'account.</span><span class="sxs-lookup"><span data-stu-id="f7da9-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="f7da9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7da9-109">EXAMPLES</span></span>

### <span data-ttu-id="f7da9-110">Esempio 1: recuperare una specifica regola del firewall</span><span class="sxs-lookup"><span data-stu-id="f7da9-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="f7da9-111">Restituisce la regola del firewall denominata "MyFirewallRule" dall'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="f7da9-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="f7da9-112">Esempio 2: elencare tutte le regole del firewall in un account</span><span class="sxs-lookup"><span data-stu-id="f7da9-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="f7da9-113">Restituisce tutte le regole del firewall nell'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="f7da9-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="f7da9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7da9-114">PARAMETERS</span></span>

### <span data-ttu-id="f7da9-115">-Account</span><span class="sxs-lookup"><span data-stu-id="f7da9-115">-Account</span></span>
<span data-ttu-id="f7da9-116">L'account di data Lake Store per recuperare la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="f7da9-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="f7da9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7da9-117">-DefaultProfile</span></span>
<span data-ttu-id="f7da9-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f7da9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7da9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7da9-119">-Name</span></span>
<span data-ttu-id="f7da9-120">Nome della regola del firewall da recuperare</span><span class="sxs-lookup"><span data-stu-id="f7da9-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="f7da9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7da9-121">-ResourceGroupName</span></span>
<span data-ttu-id="f7da9-122">Nome del gruppo di risorse in cui si vuole recuperare la regola del firewall specificata dell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="f7da9-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="f7da9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7da9-123">CommonParameters</span></span>
<span data-ttu-id="f7da9-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7da9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7da9-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7da9-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7da9-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7da9-126">INPUTS</span></span>

### <span data-ttu-id="f7da9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f7da9-127">System.String</span></span>

## <span data-ttu-id="f7da9-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7da9-128">OUTPUTS</span></span>

### <span data-ttu-id="f7da9-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f7da9-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="f7da9-130">Note</span><span class="sxs-lookup"><span data-stu-id="f7da9-130">NOTES</span></span>

## <span data-ttu-id="f7da9-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7da9-131">RELATED LINKS</span></span>
