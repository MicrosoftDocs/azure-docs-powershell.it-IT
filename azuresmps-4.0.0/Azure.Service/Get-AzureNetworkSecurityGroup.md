---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4E19A767-8233-42A0-95C5-1547B4DF297E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c08105f8083b6b2e132c3b8e61c92627572305
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029796"
---
# <span data-ttu-id="8f89d-101">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8f89d-101">Get-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="8f89d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8f89d-102">SYNOPSIS</span></span>
<span data-ttu-id="8f89d-103">Ottiene i dettagli per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="8f89d-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="8f89d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f89d-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroup [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8f89d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f89d-105">DESCRIPTION</span></span>
<span data-ttu-id="8f89d-106">Il cmdlet **Get-AzureNetworkSecurityGroup** restituisce i dettagli per un gruppo di sicurezza di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="8f89d-106">The **Get-AzureNetworkSecurityGroup** cmdlet returns details for an Azure network security group.</span></span>
<span data-ttu-id="8f89d-107">Specificare il parametro *dettagliato* per visualizzare le regole di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="8f89d-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="8f89d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f89d-108">EXAMPLES</span></span>

## <span data-ttu-id="8f89d-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8f89d-109">PARAMETERS</span></span>

### <span data-ttu-id="8f89d-110">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="8f89d-110">-Detailed</span></span>
<span data-ttu-id="8f89d-111">Indica che questo cmdlet restituisce le regole di sicurezza della rete per il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="8f89d-111">Indicates that this cmdlet returns the network security rules for the network security group.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f89d-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f89d-112">-Name</span></span>
<span data-ttu-id="8f89d-113">Specifica il nome del gruppo di sicurezza di rete ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f89d-113">Specifies the name of the network security group that this cmdlet gets.</span></span>

> [!NOTE]
> <span data-ttu-id="8f89d-114">Quando un gruppo di sicurezza di rete classico viene creato in un gruppo di risorse diverso da quello ***predefinito*** tramite il portale di Azure, è necessario usare la sintassi di PowerShell seguente: `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'` .</span><span class="sxs-lookup"><span data-stu-id="8f89d-114">When a classic network security group is created in a resource group other than ***Default-Networking*** using the Azure portal, you must use the following PowerShell syntax: `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f89d-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="8f89d-115">-Profile</span></span>
<span data-ttu-id="8f89d-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f89d-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8f89d-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8f89d-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f89d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f89d-118">CommonParameters</span></span>
<span data-ttu-id="8f89d-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f89d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f89d-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f89d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f89d-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8f89d-121">INPUTS</span></span>

## <span data-ttu-id="8f89d-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f89d-122">OUTPUTS</span></span>

## <span data-ttu-id="8f89d-123">Note</span><span class="sxs-lookup"><span data-stu-id="8f89d-123">NOTES</span></span>

## <span data-ttu-id="8f89d-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f89d-124">RELATED LINKS</span></span>

[<span data-ttu-id="8f89d-125">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8f89d-125">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="8f89d-126">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8f89d-126">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)

