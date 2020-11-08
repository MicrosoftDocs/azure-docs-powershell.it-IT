---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclustername
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
ms.openlocfilehash: c6b2f462ac66ab48b50e7555a3b5bf7c844aae3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019073"
---
# <span data-ttu-id="5acdd-101">Test-AzKustoClusterName</span><span class="sxs-lookup"><span data-stu-id="5acdd-101">Test-AzKustoClusterName</span></span>

## <span data-ttu-id="5acdd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5acdd-102">SYNOPSIS</span></span>
<span data-ttu-id="5acdd-103">Verificare se è disponibile un nome di cluster kusto specifico.</span><span class="sxs-lookup"><span data-stu-id="5acdd-103">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="5acdd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5acdd-104">SYNTAX</span></span>

```
Test-AzKustoClusterName -Location <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5acdd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5acdd-105">DESCRIPTION</span></span>
<span data-ttu-id="5acdd-106">Verificare se è disponibile un nome di cluster kusto specifico.</span><span class="sxs-lookup"><span data-stu-id="5acdd-106">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="5acdd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5acdd-107">EXAMPLES</span></span>

### <span data-ttu-id="5acdd-108">Esempio 1-verificare la disponibilità di un nome di cluster kusto in uso</span><span class="sxs-lookup"><span data-stu-id="5acdd-108">Example 1 - Check the availability of a Kusto cluster name which is in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
False                   mykustocluster      Name 'mykustocluster' with type Engine is already taken. Please specify a different name
```

<span data-ttu-id="5acdd-109">Il comando precedente restituisce un risultato che indica se un cluster kusto denominato "mykustocluster" è presente nell'area "Stati Uniti centrali".</span><span class="sxs-lookup"><span data-stu-id="5acdd-109">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

### <span data-ttu-id="5acdd-110">Esempio 2-verificare la disponibilità di un nome di cluster kusto non in uso</span><span class="sxs-lookup"><span data-stu-id="5acdd-110">Example 2 - Check the availability of a Kusto cluster name which is not in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
 True                   mykustocluster
```

<span data-ttu-id="5acdd-111">Il comando precedente restituisce un risultato che indica se un cluster kusto denominato "mykustocluster" è presente nell'area "Stati Uniti centrali".</span><span class="sxs-lookup"><span data-stu-id="5acdd-111">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

## <span data-ttu-id="5acdd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5acdd-112">PARAMETERS</span></span>

### <span data-ttu-id="5acdd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5acdd-113">-DefaultProfile</span></span>
<span data-ttu-id="5acdd-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5acdd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5acdd-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5acdd-115">-Location</span></span>
<span data-ttu-id="5acdd-116">Posizione in cui effettuare il controllo.</span><span class="sxs-lookup"><span data-stu-id="5acdd-116">The location where to check.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5acdd-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5acdd-117">-Name</span></span>
<span data-ttu-id="5acdd-118">Nome di un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="5acdd-118">Name of a specific cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5acdd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5acdd-119">CommonParameters</span></span>
<span data-ttu-id="5acdd-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5acdd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5acdd-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5acdd-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5acdd-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5acdd-122">INPUTS</span></span>

### <span data-ttu-id="5acdd-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5acdd-123">None</span></span>

## <span data-ttu-id="5acdd-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5acdd-124">OUTPUTS</span></span>

### <span data-ttu-id="5acdd-125">Microsoft. Azure. Commands. kusto. Models. PSKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="5acdd-125">Microsoft.Azure.Commands.Kusto.Models.PSKustoClusterNameAvailability</span></span>

## <span data-ttu-id="5acdd-126">Note</span><span class="sxs-lookup"><span data-stu-id="5acdd-126">NOTES</span></span>

## <span data-ttu-id="5acdd-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5acdd-127">RELATED LINKS</span></span>
