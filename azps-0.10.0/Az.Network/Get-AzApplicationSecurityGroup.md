---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: b23901a79262f4eb63e34b99c10b82442cb2fe6a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860838"
---
# <span data-ttu-id="2b169-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2b169-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="2b169-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b169-102">SYNOPSIS</span></span>
<span data-ttu-id="2b169-103">Ottiene un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2b169-103">Gets an application security group.</span></span>

## <span data-ttu-id="2b169-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b169-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b169-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b169-105">DESCRIPTION</span></span>
<span data-ttu-id="2b169-106">Il cmdlet **Get-AzApplicationSecurityGroup** ottiene un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2b169-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="2b169-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b169-107">EXAMPLES</span></span>

### <span data-ttu-id="2b169-108">Esempio 1: recuperare tutti i gruppi di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2b169-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup
```

<span data-ttu-id="2b169-109">Il comando precedente restituisce tutti i gruppi di sicurezza dell'applicazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2b169-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="2b169-110">Esempio 2: recuperare i gruppi di sicurezza delle applicazioni in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2b169-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="2b169-111">Il comando precedente restituisce tutti i gruppi di sicurezza dell'applicazione che appartengono al gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2b169-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="2b169-112">Esempio 3: recuperare un gruppo di sicurezza dell'applicazione specifico.</span><span class="sxs-lookup"><span data-stu-id="2b169-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="2b169-113">Il comando precedente restituisce il gruppo di sicurezza dell'applicazione MyApplicationSecurityGroup nel gruppo risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2b169-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="2b169-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b169-114">PARAMETERS</span></span>

### <span data-ttu-id="2b169-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b169-115">-DefaultProfile</span></span>
<span data-ttu-id="2b169-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b169-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b169-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b169-117">-Name</span></span>
<span data-ttu-id="2b169-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2b169-118">The resource name.</span></span>

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

### <span data-ttu-id="2b169-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b169-119">-ResourceGroupName</span></span>
<span data-ttu-id="2b169-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2b169-120">The resource group name.</span></span>

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

### <span data-ttu-id="2b169-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b169-121">CommonParameters</span></span>
<span data-ttu-id="2b169-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b169-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b169-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b169-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b169-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b169-124">INPUTS</span></span>

### <span data-ttu-id="2b169-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2b169-125">System.String</span></span>

## <span data-ttu-id="2b169-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b169-126">OUTPUTS</span></span>

### <span data-ttu-id="2b169-127">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2b169-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="2b169-128">Note</span><span class="sxs-lookup"><span data-stu-id="2b169-128">NOTES</span></span>

## <span data-ttu-id="2b169-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b169-129">RELATED LINKS</span></span>

[<span data-ttu-id="2b169-130">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2b169-130">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="2b169-131">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2b169-131">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="2b169-132">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2b169-132">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="2b169-133">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2b169-133">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
