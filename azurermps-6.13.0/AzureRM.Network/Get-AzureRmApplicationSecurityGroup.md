---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 49c7a9a28da7822423e43ee655b1ff2256e957e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686908"
---
# <span data-ttu-id="7dc67-101">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7dc67-101">Get-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="7dc67-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7dc67-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc67-103">Ottiene un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7dc67-103">Gets an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dc67-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7dc67-104">SYNTAX</span></span>

```
Get-AzureRmApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dc67-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7dc67-105">DESCRIPTION</span></span>
<span data-ttu-id="7dc67-106">Il cmdlet **Get-AzureRmApplicationSecurityGroup** ottiene un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7dc67-106">The **Get-AzureRmApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="7dc67-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7dc67-107">EXAMPLES</span></span>

### <span data-ttu-id="7dc67-108">Esempio 1: recuperare tutti i gruppi di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7dc67-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup
```

<span data-ttu-id="7dc67-109">Il comando precedente restituisce tutti i gruppi di sicurezza dell'applicazione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7dc67-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="7dc67-110">Esempio 2: recuperare i gruppi di sicurezza delle applicazioni in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7dc67-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="7dc67-111">Il comando precedente restituisce tutti i gruppi di sicurezza dell'applicazione che appartengono al gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7dc67-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="7dc67-112">Esempio 3: recuperare un gruppo di sicurezza dell'applicazione specifico.</span><span class="sxs-lookup"><span data-stu-id="7dc67-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="7dc67-113">Il comando precedente restituisce il gruppo di sicurezza dell'applicazione MyApplicationSecurityGroup nel gruppo risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7dc67-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="7dc67-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7dc67-114">PARAMETERS</span></span>

### <span data-ttu-id="7dc67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc67-115">-DefaultProfile</span></span>
<span data-ttu-id="7dc67-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7dc67-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dc67-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7dc67-117">-Name</span></span>
<span data-ttu-id="7dc67-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7dc67-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dc67-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dc67-119">-ResourceGroupName</span></span>
<span data-ttu-id="7dc67-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7dc67-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dc67-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc67-121">CommonParameters</span></span>
<span data-ttu-id="7dc67-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dc67-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc67-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dc67-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc67-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7dc67-124">INPUTS</span></span>

### <span data-ttu-id="7dc67-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7dc67-125">System.String</span></span>

## <span data-ttu-id="7dc67-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7dc67-126">OUTPUTS</span></span>

### <span data-ttu-id="7dc67-127">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7dc67-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="7dc67-128">Note</span><span class="sxs-lookup"><span data-stu-id="7dc67-128">NOTES</span></span>

## <span data-ttu-id="7dc67-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7dc67-129">RELATED LINKS</span></span>

[<span data-ttu-id="7dc67-130">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7dc67-130">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="7dc67-131">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7dc67-131">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="7dc67-132">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7dc67-132">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7dc67-133">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7dc67-133">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)
