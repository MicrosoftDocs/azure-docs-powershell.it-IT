---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 82ff7d915a7ddc2d15655513dade28fc1e7ffff0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192774"
---
# <span data-ttu-id="ed3de-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="ed3de-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="ed3de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed3de-102">SYNOPSIS</span></span>
<span data-ttu-id="ed3de-103">Definire un nuovo criterio di breakout del traffico di Office 365 da usare con un sito di Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="ed3de-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="ed3de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed3de-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed3de-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed3de-105">DESCRIPTION</span></span>
<span data-ttu-id="ed3de-106">Il comando New-AzOffice365PolicyProperties definisce un criterio di breakout di Office 365 che deve essere usato woith un sito Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="ed3de-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used woith a Virtual Appliance site.</span></span> 

## <span data-ttu-id="ed3de-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed3de-107">EXAMPLES</span></span>

### <span data-ttu-id="ed3de-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ed3de-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="ed3de-109">Creare un oggetto Criteri di breakout del traffico di Office 365 da usare con i comandi del sito Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="ed3de-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="ed3de-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed3de-110">PARAMETERS</span></span>

### <span data-ttu-id="ed3de-111">-Consenti</span><span class="sxs-lookup"><span data-stu-id="ed3de-111">-Allow</span></span>
<span data-ttu-id="ed3de-112">Breakout il traffico della categoria Consenti.</span><span class="sxs-lookup"><span data-stu-id="ed3de-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="ed3de-113">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="ed3de-113">-Default</span></span>
<span data-ttu-id="ed3de-114">Breakout il traffico delle categorie predefinito.</span><span class="sxs-lookup"><span data-stu-id="ed3de-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="ed3de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed3de-115">-DefaultProfile</span></span>
<span data-ttu-id="ed3de-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed3de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed3de-117">-Optimize</span><span class="sxs-lookup"><span data-stu-id="ed3de-117">-Optimize</span></span>
<span data-ttu-id="ed3de-118">Breakout il traffico di categoria optimize.</span><span class="sxs-lookup"><span data-stu-id="ed3de-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="ed3de-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed3de-119">CommonParameters</span></span>
<span data-ttu-id="ed3de-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed3de-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed3de-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed3de-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed3de-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed3de-122">INPUTS</span></span>

### <span data-ttu-id="ed3de-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ed3de-123">None</span></span>

## <span data-ttu-id="ed3de-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed3de-124">OUTPUTS</span></span>

### <span data-ttu-id="ed3de-125">Microsoft. Azure. Commands. Network. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="ed3de-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="ed3de-126">Note</span><span class="sxs-lookup"><span data-stu-id="ed3de-126">NOTES</span></span>

## <span data-ttu-id="ed3de-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed3de-127">RELATED LINKS</span></span>
