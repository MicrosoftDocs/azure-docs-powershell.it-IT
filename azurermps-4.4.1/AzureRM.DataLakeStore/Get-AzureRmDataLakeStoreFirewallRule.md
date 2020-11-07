---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 8c7d936f8ea64534016286e97b34d36f41a72cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687218"
---
# <span data-ttu-id="49316-101">Get-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="49316-101">Get-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="49316-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49316-102">SYNOPSIS</span></span>
<span data-ttu-id="49316-103">Ottiene le regole del firewall specificate nello Store Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="49316-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="49316-104">Se non è specificata alcuna regola del firewall, elenca tutte le regole del firewall per l'account.</span><span class="sxs-lookup"><span data-stu-id="49316-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49316-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49316-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49316-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49316-106">DESCRIPTION</span></span>
<span data-ttu-id="49316-107">Il cmdlet Get-AzureRmDataLakeStoreFirewallRule ottiene le regole del firewall specificate nello Store Data Lake specificato.</span><span class="sxs-lookup"><span data-stu-id="49316-107">The Get-AzureRmDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="49316-108">Se non è specificata alcuna regola del firewall, elenca tutte le regole del firewall per l'account.</span><span class="sxs-lookup"><span data-stu-id="49316-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="49316-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49316-109">EXAMPLES</span></span>

### <span data-ttu-id="49316-110">Esempio 1: recuperare una specifica regola del firewall</span><span class="sxs-lookup"><span data-stu-id="49316-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="49316-111">Restituisce la regola del firewall denominata "MyFirewallRule" dall'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="49316-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="49316-112">Esempio 2: elencare tutte le regole del firewall in un account</span><span class="sxs-lookup"><span data-stu-id="49316-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="49316-113">Restituisce tutte le regole del firewall nell'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="49316-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="49316-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49316-114">PARAMETERS</span></span>

### <span data-ttu-id="49316-115">-Account</span><span class="sxs-lookup"><span data-stu-id="49316-115">-Account</span></span>
<span data-ttu-id="49316-116">L'account di data Lake Store per recuperare la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="49316-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="49316-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="49316-117">-Name</span></span>
<span data-ttu-id="49316-118">Nome della regola del firewall da recuperare</span><span class="sxs-lookup"><span data-stu-id="49316-118">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="49316-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49316-119">-ResourceGroupName</span></span>
<span data-ttu-id="49316-120">Nome del gruppo di risorse in cui si vuole recuperare la regola del firewall specificata dell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="49316-120">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="49316-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49316-121">-DefaultProfile</span></span>
<span data-ttu-id="49316-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49316-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49316-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49316-123">CommonParameters</span></span>
<span data-ttu-id="49316-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49316-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49316-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49316-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49316-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49316-126">INPUTS</span></span>

## <span data-ttu-id="49316-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49316-127">OUTPUTS</span></span>

### <span data-ttu-id="49316-128">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="49316-128">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="49316-129">Regola del firewall specificata da recuperare</span><span class="sxs-lookup"><span data-stu-id="49316-129">The specified firewall rule to retrieve</span></span>

### <span data-ttu-id="49316-130">IList<DataLakeStoreFirewallRule></span><span class="sxs-lookup"><span data-stu-id="49316-130">IList<DataLakeStoreFirewallRule></span></span>
<span data-ttu-id="49316-131">Elenco delle regole del firewall nell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="49316-131">The list of firewall rules in the specified account.</span></span>

## <span data-ttu-id="49316-132">Note</span><span class="sxs-lookup"><span data-stu-id="49316-132">NOTES</span></span>

## <span data-ttu-id="49316-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49316-133">RELATED LINKS</span></span>

