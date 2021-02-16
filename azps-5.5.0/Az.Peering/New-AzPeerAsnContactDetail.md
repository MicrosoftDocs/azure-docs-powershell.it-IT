---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184038"
---
# <span data-ttu-id="beaaa-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="beaaa-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="beaaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beaaa-102">SYNOPSIS</span></span>
<span data-ttu-id="beaaa-103">Crea un dettaglio di contatto in memoria per PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="beaaa-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="beaaa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="beaaa-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="beaaa-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="beaaa-105">DESCRIPTION</span></span>
<span data-ttu-id="beaaa-106">Creare un dettaglio di contatto PeerAsn in memoria.</span><span class="sxs-lookup"><span data-stu-id="beaaa-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="beaaa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="beaaa-107">EXAMPLES</span></span>

### <span data-ttu-id="beaaa-108">Creare i dettagli del contatto e aggiungerli a PeerAsn</span><span class="sxs-lookup"><span data-stu-id="beaaa-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="beaaa-109">Sono necessari il ruolo e la posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="beaaa-109">Role and email are required.</span></span> <span data-ttu-id="beaaa-110">Il telefono è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="beaaa-110">Phone is optional.</span></span> <span data-ttu-id="beaaa-111">Il telefono supporta +-() o spazi.</span><span class="sxs-lookup"><span data-stu-id="beaaa-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="beaaa-112">Un PeerAsn deve includere almeno un dettaglio di contatto di tipo "Noc"</span><span class="sxs-lookup"><span data-stu-id="beaaa-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="beaaa-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="beaaa-113">PARAMETERS</span></span>

### <span data-ttu-id="beaaa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beaaa-114">-DefaultProfile</span></span>
<span data-ttu-id="beaaa-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="beaaa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="beaaa-116">-E-mail</span><span class="sxs-lookup"><span data-stu-id="beaaa-116">-Email</span></span>
<span data-ttu-id="beaaa-117">Indirizzi di posta elettronica usati per contattare in caso di problemi in genere un Network Operations Center</span><span class="sxs-lookup"><span data-stu-id="beaaa-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="beaaa-118">-Telefono</span><span class="sxs-lookup"><span data-stu-id="beaaa-118">-Phone</span></span>
<span data-ttu-id="beaaa-119">Telefono usato per contattare in caso di problemi che in genere si verificano in un Network Operations Center</span><span class="sxs-lookup"><span data-stu-id="beaaa-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beaaa-120">-Role</span><span class="sxs-lookup"><span data-stu-id="beaaa-120">-Role</span></span>
<span data-ttu-id="beaaa-121">Scegliere il ruolo più adatto alle informazioni di contatto.</span><span class="sxs-lookup"><span data-stu-id="beaaa-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="beaaa-122">Il contatto NOC è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="beaaa-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="beaaa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beaaa-123">CommonParameters</span></span>
<span data-ttu-id="beaaa-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beaaa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beaaa-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="beaaa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beaaa-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="beaaa-126">INPUTS</span></span>

### <span data-ttu-id="beaaa-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="beaaa-127">None</span></span>

## <span data-ttu-id="beaaa-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="beaaa-128">OUTPUTS</span></span>

### <span data-ttu-id="beaaa-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="beaaa-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="beaaa-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="beaaa-130">NOTES</span></span>

## <span data-ttu-id="beaaa-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="beaaa-131">RELATED LINKS</span></span>
