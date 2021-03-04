---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: a2b3a4878db022018bd0fae1d8e43e3700dd5e35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958365"
---
# <span data-ttu-id="bce17-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="bce17-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="bce17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bce17-102">SYNOPSIS</span></span>
<span data-ttu-id="bce17-103">Creare un oggetto criterio di interruzione del traffico di Office 365.</span><span class="sxs-lookup"><span data-stu-id="bce17-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="bce17-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bce17-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bce17-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bce17-105">DESCRIPTION</span></span>
<span data-ttu-id="bce17-106">Creare un criterio di interruzione di Office 365 da usare con i cmdlet New-AzVpnSite Update-AzVpnSite distribuzione.</span><span class="sxs-lookup"><span data-stu-id="bce17-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="bce17-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bce17-107">EXAMPLES</span></span>

### <span data-ttu-id="bce17-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bce17-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="bce17-109">Creare un criterio di interruzione del traffico di Office 365 con il sottoassempio consentito per consentire e ottimizzare la categoria di traffico.</span><span class="sxs-lookup"><span data-stu-id="bce17-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="bce17-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bce17-110">PARAMETERS</span></span>

### <span data-ttu-id="bce17-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="bce17-111">-Allow</span></span>
<span data-ttu-id="bce17-112">Breakout the allow category traffic.</span><span class="sxs-lookup"><span data-stu-id="bce17-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="bce17-113">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="bce17-113">-Default</span></span>
<span data-ttu-id="bce17-114">Suddividere il traffico della categoria predefinita.</span><span class="sxs-lookup"><span data-stu-id="bce17-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="bce17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce17-115">-DefaultProfile</span></span>
<span data-ttu-id="bce17-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bce17-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bce17-117">-Optimize</span><span class="sxs-lookup"><span data-stu-id="bce17-117">-Optimize</span></span>
<span data-ttu-id="bce17-118">Suddividere la sezione Ottimizza il traffico della categoria.</span><span class="sxs-lookup"><span data-stu-id="bce17-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="bce17-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce17-119">CommonParameters</span></span>
<span data-ttu-id="bce17-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bce17-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce17-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bce17-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce17-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="bce17-122">INPUTS</span></span>

### <span data-ttu-id="bce17-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bce17-123">None</span></span>

## <span data-ttu-id="bce17-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bce17-124">OUTPUTS</span></span>

### <span data-ttu-id="bce17-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="bce17-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="bce17-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="bce17-126">NOTES</span></span>

## <span data-ttu-id="bce17-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bce17-127">RELATED LINKS</span></span>
