---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336088"
---
# <span data-ttu-id="f6657-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="f6657-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="f6657-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6657-102">SYNOPSIS</span></span>
<span data-ttu-id="f6657-103">Crea un dettaglio di contatto in memoria per PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="f6657-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="f6657-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6657-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6657-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6657-105">DESCRIPTION</span></span>
<span data-ttu-id="f6657-106">Creare un dettaglio di contatto PeerAsn in memoria.</span><span class="sxs-lookup"><span data-stu-id="f6657-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="f6657-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6657-107">EXAMPLES</span></span>

### <span data-ttu-id="f6657-108">Creare dettagli di contatto e aggiungere a PeerAsn</span><span class="sxs-lookup"><span data-stu-id="f6657-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="f6657-109">Ruolo e posta elettronica sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="f6657-109">Role and email are required.</span></span> <span data-ttu-id="f6657-110">Il telefono è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f6657-110">Phone is optional.</span></span> <span data-ttu-id="f6657-111">Il telefono supporta +-() o gli spazi.</span><span class="sxs-lookup"><span data-stu-id="f6657-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="f6657-112">Un PeerAsn deve includere almeno un dettaglio di contatto di tipo "NOC"</span><span class="sxs-lookup"><span data-stu-id="f6657-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="f6657-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6657-113">PARAMETERS</span></span>

### <span data-ttu-id="f6657-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6657-114">-DefaultProfile</span></span>
<span data-ttu-id="f6657-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6657-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6657-116">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="f6657-116">-Email</span></span>
<span data-ttu-id="f6657-117">Indirizzi di posta elettronica usati per contattare i problemi di arrise in genere un centro operazioni di rete</span><span class="sxs-lookup"><span data-stu-id="f6657-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="f6657-118">-Telefono</span><span class="sxs-lookup"><span data-stu-id="f6657-118">-Phone</span></span>
<span data-ttu-id="f6657-119">Telefono usato per contattare i problemi di arrise in genere un centro operazioni di rete</span><span class="sxs-lookup"><span data-stu-id="f6657-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="f6657-120">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="f6657-120">-Role</span></span>
<span data-ttu-id="f6657-121">Scegliere il ruolo più adatto alle informazioni di contatto.</span><span class="sxs-lookup"><span data-stu-id="f6657-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="f6657-122">Il contatto NOC è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f6657-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="f6657-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6657-123">CommonParameters</span></span>
<span data-ttu-id="f6657-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6657-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6657-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6657-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6657-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6657-126">INPUTS</span></span>

### <span data-ttu-id="f6657-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f6657-127">None</span></span>

## <span data-ttu-id="f6657-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6657-128">OUTPUTS</span></span>

### <span data-ttu-id="f6657-129">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="f6657-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="f6657-130">Note</span><span class="sxs-lookup"><span data-stu-id="f6657-130">NOTES</span></span>

## <span data-ttu-id="f6657-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6657-131">RELATED LINKS</span></span>
