---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9fae8c6d543bddc3ad4110b95a1c1b4a1f146879
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301944"
---
# <span data-ttu-id="c3db8-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="c3db8-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="c3db8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3db8-102">SYNOPSIS</span></span>
<span data-ttu-id="c3db8-103">Definire un nuovo criterio di breakout del traffico di Office 365 da usare con un sito di Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="c3db8-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="c3db8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3db8-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3db8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3db8-105">DESCRIPTION</span></span>
<span data-ttu-id="c3db8-106">Il comando New-AzOffice365PolicyProperties definisce un criterio di breakout di Office 365 che deve essere usato con un sito Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="c3db8-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="c3db8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3db8-107">EXAMPLES</span></span>

### <span data-ttu-id="c3db8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c3db8-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="c3db8-109">Creare un oggetto Criteri di breakout del traffico di Office 365 da usare con i comandi del sito Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="c3db8-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="c3db8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3db8-110">PARAMETERS</span></span>

### <span data-ttu-id="c3db8-111">-Consenti</span><span class="sxs-lookup"><span data-stu-id="c3db8-111">-Allow</span></span>
<span data-ttu-id="c3db8-112">Breakout il traffico della categoria Consenti.</span><span class="sxs-lookup"><span data-stu-id="c3db8-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="c3db8-113">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="c3db8-113">-Default</span></span>
<span data-ttu-id="c3db8-114">Breakout il traffico delle categorie predefinito.</span><span class="sxs-lookup"><span data-stu-id="c3db8-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="c3db8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3db8-115">-DefaultProfile</span></span>
<span data-ttu-id="c3db8-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3db8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3db8-117">-Optimize</span><span class="sxs-lookup"><span data-stu-id="c3db8-117">-Optimize</span></span>
<span data-ttu-id="c3db8-118">Breakout il traffico di categoria optimize.</span><span class="sxs-lookup"><span data-stu-id="c3db8-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="c3db8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3db8-119">CommonParameters</span></span>
<span data-ttu-id="c3db8-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3db8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3db8-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3db8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3db8-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3db8-122">INPUTS</span></span>

### <span data-ttu-id="c3db8-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c3db8-123">None</span></span>

## <span data-ttu-id="c3db8-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3db8-124">OUTPUTS</span></span>

### <span data-ttu-id="c3db8-125">Microsoft. Azure. Commands. Network. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="c3db8-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="c3db8-126">Note</span><span class="sxs-lookup"><span data-stu-id="c3db8-126">NOTES</span></span>

## <span data-ttu-id="c3db8-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3db8-127">RELATED LINKS</span></span>
