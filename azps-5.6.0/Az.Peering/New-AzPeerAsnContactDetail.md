---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: 978c513646c08577f4fa15b8a0e460320878c7c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989448"
---
# <span data-ttu-id="e8578-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="e8578-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="e8578-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8578-102">SYNOPSIS</span></span>
<span data-ttu-id="e8578-103">Crea un dettaglio di contatto in memoria per PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="e8578-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="e8578-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8578-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8578-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e8578-105">DESCRIPTION</span></span>
<span data-ttu-id="e8578-106">Creare un dettaglio di contatto PeerAsn in memoria.</span><span class="sxs-lookup"><span data-stu-id="e8578-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="e8578-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8578-107">EXAMPLES</span></span>

### <span data-ttu-id="e8578-108">Creare i dettagli del contatto e aggiungerli a PeerAsn</span><span class="sxs-lookup"><span data-stu-id="e8578-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="e8578-109">Sono necessari ruolo e posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="e8578-109">Role and email are required.</span></span> <span data-ttu-id="e8578-110">Il telefono è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e8578-110">Phone is optional.</span></span> <span data-ttu-id="e8578-111">Il telefono supporta +-() o spazi.</span><span class="sxs-lookup"><span data-stu-id="e8578-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="e8578-112">Un PeerAsn deve includere almeno un dettaglio di contatto di tipo "Noc"</span><span class="sxs-lookup"><span data-stu-id="e8578-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="e8578-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8578-113">PARAMETERS</span></span>

### <span data-ttu-id="e8578-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8578-114">-DefaultProfile</span></span>
<span data-ttu-id="e8578-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8578-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8578-116">-E-mail</span><span class="sxs-lookup"><span data-stu-id="e8578-116">-Email</span></span>
<span data-ttu-id="e8578-117">Indirizzi di posta elettronica usati per contattare in caso di problemi in genere un Network Operations Center</span><span class="sxs-lookup"><span data-stu-id="e8578-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="e8578-118">-Telefono</span><span class="sxs-lookup"><span data-stu-id="e8578-118">-Phone</span></span>
<span data-ttu-id="e8578-119">Telefono usato per contattare in caso di problemi che in genere si verificano in un Network Operations Center</span><span class="sxs-lookup"><span data-stu-id="e8578-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="e8578-120">-Role</span><span class="sxs-lookup"><span data-stu-id="e8578-120">-Role</span></span>
<span data-ttu-id="e8578-121">Scegliere il ruolo più adatto alle informazioni di contatto.</span><span class="sxs-lookup"><span data-stu-id="e8578-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="e8578-122">Il contatto NOC è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e8578-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="e8578-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8578-123">CommonParameters</span></span>
<span data-ttu-id="e8578-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8578-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8578-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e8578-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8578-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="e8578-126">INPUTS</span></span>

### <span data-ttu-id="e8578-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e8578-127">None</span></span>

## <span data-ttu-id="e8578-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8578-128">OUTPUTS</span></span>

### <span data-ttu-id="e8578-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="e8578-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="e8578-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="e8578-130">NOTES</span></span>

## <span data-ttu-id="e8578-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8578-131">RELATED LINKS</span></span>
