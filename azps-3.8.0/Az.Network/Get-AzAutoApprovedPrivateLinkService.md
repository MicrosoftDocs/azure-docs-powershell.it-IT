---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: b03aad1f76c5151746d50e69bc48ccf10e60842f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864407"
---
# <span data-ttu-id="37350-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="37350-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="37350-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37350-102">SYNOPSIS</span></span>
<span data-ttu-id="37350-103">Ottiene una matrice di ID del servizio di collegamento privato che può essere collegata a un punto finale privato con l'approvazione automatica.</span><span class="sxs-lookup"><span data-stu-id="37350-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="37350-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37350-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37350-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37350-105">DESCRIPTION</span></span>
<span data-ttu-id="37350-106">**Get-AzAutoApprovedPrivateLinkService** ottiene una matrice di ID del servizio di collegamento privato che può essere collegata a un punto finale privato con l'approvazione automatica.</span><span class="sxs-lookup"><span data-stu-id="37350-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="37350-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37350-107">EXAMPLES</span></span>

### <span data-ttu-id="37350-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="37350-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="37350-109">In questo esempio viene restituita una matrice di ID del servizio di collegamento privato che può essere collegata a un punto finale privato con l'approvazione automatica.</span><span class="sxs-lookup"><span data-stu-id="37350-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="37350-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37350-110">PARAMETERS</span></span>

### <span data-ttu-id="37350-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37350-111">-DefaultProfile</span></span>
<span data-ttu-id="37350-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37350-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37350-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="37350-113">-Location</span></span>
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

### <span data-ttu-id="37350-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37350-114">-ResourceGroupName</span></span>
<span data-ttu-id="37350-115">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="37350-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="37350-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37350-116">CommonParameters</span></span>
<span data-ttu-id="37350-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37350-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37350-118">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37350-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37350-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37350-119">INPUTS</span></span>

### <span data-ttu-id="37350-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="37350-120">None</span></span>

## <span data-ttu-id="37350-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37350-121">OUTPUTS</span></span>

### <span data-ttu-id="37350-122">Microsoft. Azure. Commands. Network. Models. PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="37350-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="37350-123">Note</span><span class="sxs-lookup"><span data-stu-id="37350-123">NOTES</span></span>

## <span data-ttu-id="37350-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37350-124">RELATED LINKS</span></span>
