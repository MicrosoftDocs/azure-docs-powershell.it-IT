---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: 2aeb26447c5684b57d966c403a256fe3d1361a41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192776"
---
# <span data-ttu-id="ba086-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="ba086-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="ba086-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba086-102">SYNOPSIS</span></span>
<span data-ttu-id="ba086-103">Creare un oggetto Criteri di breakout del traffico di Office 365.</span><span class="sxs-lookup"><span data-stu-id="ba086-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="ba086-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba086-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba086-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba086-105">DESCRIPTION</span></span>
<span data-ttu-id="ba086-106">Creare un criterio di breakout di Office 365 da usare con i cmdlet New-AzVpnSite e Update-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="ba086-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="ba086-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba086-107">EXAMPLES</span></span>

### <span data-ttu-id="ba086-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ba086-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="ba086-109">Creare un criterio di breakout del traffico di Office 365 con breakout consentito per consentire e ottimizzare la categoria di traffico.</span><span class="sxs-lookup"><span data-stu-id="ba086-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="ba086-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba086-110">PARAMETERS</span></span>

### <span data-ttu-id="ba086-111">-Consenti</span><span class="sxs-lookup"><span data-stu-id="ba086-111">-Allow</span></span>
<span data-ttu-id="ba086-112">Breakout il traffico della categoria Consenti.</span><span class="sxs-lookup"><span data-stu-id="ba086-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="ba086-113">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="ba086-113">-Default</span></span>
<span data-ttu-id="ba086-114">Breakout il traffico delle categorie predefinito.</span><span class="sxs-lookup"><span data-stu-id="ba086-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="ba086-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba086-115">-DefaultProfile</span></span>
<span data-ttu-id="ba086-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba086-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba086-117">-Optimize</span><span class="sxs-lookup"><span data-stu-id="ba086-117">-Optimize</span></span>
<span data-ttu-id="ba086-118">Breakout il traffico di categoria optimize.</span><span class="sxs-lookup"><span data-stu-id="ba086-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="ba086-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba086-119">CommonParameters</span></span>
<span data-ttu-id="ba086-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba086-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba086-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba086-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba086-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba086-122">INPUTS</span></span>

### <span data-ttu-id="ba086-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ba086-123">None</span></span>

## <span data-ttu-id="ba086-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba086-124">OUTPUTS</span></span>

### <span data-ttu-id="ba086-125">Microsoft. Azure. Commands. Network. Models. PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="ba086-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="ba086-126">Note</span><span class="sxs-lookup"><span data-stu-id="ba086-126">NOTES</span></span>

## <span data-ttu-id="ba086-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba086-127">RELATED LINKS</span></span>