---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 191b1ebc1f83387a9cf1ac59f6fb3f7a55f115ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509236"
---
# <span data-ttu-id="ab952-101">Get-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ab952-101">Get-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="ab952-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab952-102">SYNOPSIS</span></span>
<span data-ttu-id="ab952-103">Ottiene le regole del firewall specificate nello Store Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="ab952-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="ab952-104">Se non è specificata alcuna regola del firewall, elenca tutte le regole del firewall per l'account.</span><span class="sxs-lookup"><span data-stu-id="ab952-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab952-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab952-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab952-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab952-106">DESCRIPTION</span></span>
<span data-ttu-id="ab952-107">Il cmdlet Get-AzureRmDataLakeStoreFirewallRule ottiene le regole del firewall specificate nello Store Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="ab952-107">The Get-AzureRmDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="ab952-108">Se non è specificata alcuna regola del firewall, elenca tutte le regole del firewall per l'account.</span><span class="sxs-lookup"><span data-stu-id="ab952-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="ab952-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab952-109">EXAMPLES</span></span>

### <span data-ttu-id="ab952-110">Esempio 1: recuperare una specifica regola del firewall</span><span class="sxs-lookup"><span data-stu-id="ab952-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="ab952-111">Restituisce la regola del firewall denominata "MyFirewallRule" dall'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="ab952-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="ab952-112">Esempio 2: elencare tutte le regole del firewall in un account</span><span class="sxs-lookup"><span data-stu-id="ab952-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="ab952-113">Restituisce tutte le regole del firewall nell'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="ab952-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="ab952-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab952-114">PARAMETERS</span></span>

### <span data-ttu-id="ab952-115">-Account</span><span class="sxs-lookup"><span data-stu-id="ab952-115">-Account</span></span>
<span data-ttu-id="ab952-116">L'account di data Lake Store per recuperare la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="ab952-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="ab952-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab952-117">-DefaultProfile</span></span>
<span data-ttu-id="ab952-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ab952-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab952-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab952-119">-Name</span></span>
<span data-ttu-id="ab952-120">Nome della regola del firewall da recuperare</span><span class="sxs-lookup"><span data-stu-id="ab952-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="ab952-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab952-121">-ResourceGroupName</span></span>
<span data-ttu-id="ab952-122">Nome del gruppo di risorse in cui si vuole recuperare la regola del firewall specificata dell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="ab952-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="ab952-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab952-123">CommonParameters</span></span>
<span data-ttu-id="ab952-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab952-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab952-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab952-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab952-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab952-126">INPUTS</span></span>

### <span data-ttu-id="ab952-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ab952-127">System.String</span></span>

## <span data-ttu-id="ab952-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab952-128">OUTPUTS</span></span>

### <span data-ttu-id="ab952-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ab952-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="ab952-130">Note</span><span class="sxs-lookup"><span data-stu-id="ab952-130">NOTES</span></span>

## <span data-ttu-id="ab952-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab952-131">RELATED LINKS</span></span>
