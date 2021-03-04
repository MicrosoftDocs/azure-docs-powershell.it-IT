---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9e48bfd243133052f526f2b9adcbef2072cdd2cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958350"
---
# <span data-ttu-id="06a2f-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="06a2f-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="06a2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="06a2f-103">Definire un nuovo criterio di interruzione del traffico di Office 365 da usare con un sito appliance virtuale.</span><span class="sxs-lookup"><span data-stu-id="06a2f-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="06a2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06a2f-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06a2f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="06a2f-105">DESCRIPTION</span></span>
<span data-ttu-id="06a2f-106">Il New-AzOffice365PolicyProperties predefinito definisce un criterio di interruzione di Office 365 da usare con un sito di appliance virtuali.</span><span class="sxs-lookup"><span data-stu-id="06a2f-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="06a2f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06a2f-107">EXAMPLES</span></span>

### <span data-ttu-id="06a2f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="06a2f-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="06a2f-109">Creare un oggetto criterio di interruzione del traffico di Office 365 da usare con i comandi del sito Appliance virtuali.</span><span class="sxs-lookup"><span data-stu-id="06a2f-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="06a2f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06a2f-110">PARAMETERS</span></span>

### <span data-ttu-id="06a2f-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="06a2f-111">-Allow</span></span>
<span data-ttu-id="06a2f-112">Breakout the allow category traffic.</span><span class="sxs-lookup"><span data-stu-id="06a2f-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="06a2f-113">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="06a2f-113">-Default</span></span>
<span data-ttu-id="06a2f-114">Suddividere il traffico della categoria predefinita.</span><span class="sxs-lookup"><span data-stu-id="06a2f-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="06a2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a2f-115">-DefaultProfile</span></span>
<span data-ttu-id="06a2f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06a2f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06a2f-117">-Optimize</span><span class="sxs-lookup"><span data-stu-id="06a2f-117">-Optimize</span></span>
<span data-ttu-id="06a2f-118">Breakout the optimize category traffic.</span><span class="sxs-lookup"><span data-stu-id="06a2f-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="06a2f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a2f-119">CommonParameters</span></span>
<span data-ttu-id="06a2f-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06a2f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a2f-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="06a2f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a2f-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="06a2f-122">INPUTS</span></span>

### <span data-ttu-id="06a2f-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="06a2f-123">None</span></span>

## <span data-ttu-id="06a2f-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06a2f-124">OUTPUTS</span></span>

### <span data-ttu-id="06a2f-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="06a2f-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="06a2f-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="06a2f-126">NOTES</span></span>

## <span data-ttu-id="06a2f-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06a2f-127">RELATED LINKS</span></span>
