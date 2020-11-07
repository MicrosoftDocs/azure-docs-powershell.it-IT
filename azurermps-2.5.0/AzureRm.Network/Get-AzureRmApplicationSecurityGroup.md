---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationsecuritygroup
schema: 2.0.0
ms.openlocfilehash: 52050426c34b30bcab867643fbb3e5b9c373f3f2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865915"
---
# <span data-ttu-id="c2cd6-101">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c2cd6-101">Get-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="c2cd6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="c2cd6-103">Ottiene un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-103">Gets an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2cd6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2cd6-104">SYNTAX</span></span>

```
Get-AzureRmApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2cd6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2cd6-105">DESCRIPTION</span></span>
<span data-ttu-id="c2cd6-106">Il cmdlet **Get-AzureRmApplicationSecurityGroup** ottiene un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-106">The **Get-AzureRmApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="c2cd6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2cd6-107">EXAMPLES</span></span>

### <span data-ttu-id="c2cd6-108">Esempio 1: recuperare tutti i gruppi di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup
```

<span data-ttu-id="c2cd6-109">Il comando precedente restituisce tutti i gruppi di sicurezza dell'applicazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="c2cd6-110">Esempio 2: recuperare i gruppi di sicurezza delle applicazioni in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="c2cd6-111">Il comando precedente restituisce tutti i gruppi di sicurezza dell'applicazione che appartengono al gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="c2cd6-112">Esempio 3: recuperare un gruppo di sicurezza dell'applicazione specifico.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="c2cd6-113">Il comando precedente restituisce il gruppo di sicurezza dell'applicazione MyApplicationSecurityGroup nel gruppo risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="c2cd6-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2cd6-114">PARAMETERS</span></span>

### <span data-ttu-id="c2cd6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2cd6-115">-DefaultProfile</span></span>
<span data-ttu-id="c2cd6-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2cd6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2cd6-117">-Name</span></span>
<span data-ttu-id="c2cd6-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2cd6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2cd6-119">-ResourceGroupName</span></span>
<span data-ttu-id="c2cd6-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2cd6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2cd6-121">CommonParameters</span></span>
<span data-ttu-id="c2cd6-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2cd6-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2cd6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2cd6-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2cd6-124">INPUTS</span></span>

### <span data-ttu-id="c2cd6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c2cd6-125">System.String</span></span>

## <span data-ttu-id="c2cd6-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2cd6-126">OUTPUTS</span></span>

### <span data-ttu-id="c2cd6-127">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c2cd6-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="c2cd6-128">Note</span><span class="sxs-lookup"><span data-stu-id="c2cd6-128">NOTES</span></span>

## <span data-ttu-id="c2cd6-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2cd6-129">RELATED LINKS</span></span>

[<span data-ttu-id="c2cd6-130">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c2cd6-130">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="c2cd6-131">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c2cd6-131">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="c2cd6-132">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c2cd6-132">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c2cd6-133">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c2cd6-133">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)
