---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
ms.openlocfilehash: 5bdd5e5d5212564afb1f9b06f220e8c452bcbbaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522040"
---
# <span data-ttu-id="94df1-101">Get-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="94df1-101">Get-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="94df1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94df1-102">SYNOPSIS</span></span>
<span data-ttu-id="94df1-103">Ottiene una risorsa di primo livello del profilo di rete esistente</span><span class="sxs-lookup"><span data-stu-id="94df1-103">Gets an existing network profile top level resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94df1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94df1-104">SYNTAX</span></span>

### <span data-ttu-id="94df1-105">NOEXPAND (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94df1-105">NoExpand (Default)</span></span>
```
Get-AzureRmNetworkProfile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94df1-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="94df1-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94df1-107">GetByResourceNameNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="94df1-107">GetByResourceNameNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile [-ResourceGroupName <String>] [-Name <String>] -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94df1-108">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="94df1-108">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94df1-109">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="94df1-109">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94df1-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94df1-110">DESCRIPTION</span></span>
<span data-ttu-id="94df1-111">Il cmdlet **Get-AzureRmNetworkProfile** recupera una risorsa di primo livello del profilo di rete esistente</span><span class="sxs-lookup"><span data-stu-id="94df1-111">The **Get-AzureRmNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="94df1-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94df1-112">EXAMPLES</span></span>

### <span data-ttu-id="94df1-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="94df1-113">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="94df1-114">In questo articolo viene recuperato il profilo di rete NP1 nel gruppo di risorse RG1</span><span class="sxs-lookup"><span data-stu-id="94df1-114">This retrieves the network profile np1 in resource group rg1</span></span>

## <span data-ttu-id="94df1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94df1-115">PARAMETERS</span></span>

### <span data-ttu-id="94df1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94df1-116">-DefaultProfile</span></span>
<span data-ttu-id="94df1-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94df1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94df1-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="94df1-118">-ExpandResource</span></span>
<span data-ttu-id="94df1-119">Riferimento alla risorsa da espandere.</span><span class="sxs-lookup"><span data-stu-id="94df1-119">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceNameNoExpandParameterSet, GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94df1-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="94df1-120">-Name</span></span>
<span data-ttu-id="94df1-121">Nome del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="94df1-121">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94df1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94df1-122">-ResourceGroupName</span></span>
<span data-ttu-id="94df1-123">Nome del gruppo di risorse del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="94df1-123">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94df1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94df1-124">-ResourceId</span></span>
<span data-ttu-id="94df1-125">ID di gestione risorse di Azure del profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="94df1-125">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94df1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94df1-126">CommonParameters</span></span>
<span data-ttu-id="94df1-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94df1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94df1-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94df1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94df1-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94df1-129">INPUTS</span></span>

### <span data-ttu-id="94df1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="94df1-130">System.String</span></span>

## <span data-ttu-id="94df1-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94df1-131">OUTPUTS</span></span>

### <span data-ttu-id="94df1-132">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="94df1-132">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="94df1-133">Note</span><span class="sxs-lookup"><span data-stu-id="94df1-133">NOTES</span></span>

## <span data-ttu-id="94df1-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94df1-134">RELATED LINKS</span></span>
