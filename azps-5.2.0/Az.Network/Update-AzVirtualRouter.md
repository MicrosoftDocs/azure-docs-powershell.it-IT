---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: d7f52ded01ce5b785c1e935ba8d3ebf4b1c0a5fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350743"
---
# <span data-ttu-id="c1b64-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="c1b64-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="c1b64-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1b64-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b64-103">Aggiorna un router virtuale.</span><span class="sxs-lookup"><span data-stu-id="c1b64-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="c1b64-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1b64-104">SYNTAX</span></span>

### <span data-ttu-id="c1b64-105">VirtualRouterNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1b64-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1b64-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1b64-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1b64-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1b64-107">DESCRIPTION</span></span>
<span data-ttu-id="c1b64-108">Aggiorna il router virtuale per abilitare o disabilitare il traffico di succursale.</span><span class="sxs-lookup"><span data-stu-id="c1b64-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="c1b64-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1b64-109">EXAMPLES</span></span>

### <span data-ttu-id="c1b64-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c1b64-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="c1b64-111">Aggiorna il router virtuale per consentire il traffico di succursale in Branch</span><span class="sxs-lookup"><span data-stu-id="c1b64-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="c1b64-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c1b64-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="c1b64-113">Aggiorna il router virtuale per bloccare il ramo al traffico di succursale</span><span class="sxs-lookup"><span data-stu-id="c1b64-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="c1b64-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1b64-114">PARAMETERS</span></span>

### <span data-ttu-id="c1b64-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="c1b64-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="c1b64-116">Contrassegna per consentire il traffico Branch to Branch per il router virtuale.</span><span class="sxs-lookup"><span data-stu-id="c1b64-116">Flag to allow branch to branch traffic for virtual router.</span></span>

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

### <span data-ttu-id="c1b64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b64-117">-DefaultProfile</span></span>
<span data-ttu-id="c1b64-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b64-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b64-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1b64-119">-ResourceGroupName</span></span>
<span data-ttu-id="c1b64-120">Il nome del gruppo di risorse del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="c1b64-120">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1b64-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1b64-121">-ResourceId</span></span>
<span data-ttu-id="c1b64-122">ResourceId del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="c1b64-122">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1b64-123">-Routername</span><span class="sxs-lookup"><span data-stu-id="c1b64-123">-RouterName</span></span>
<span data-ttu-id="c1b64-124">Nome del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="c1b64-124">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1b64-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b64-125">CommonParameters</span></span>
<span data-ttu-id="c1b64-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1b64-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b64-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1b64-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b64-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1b64-128">INPUTS</span></span>

### <span data-ttu-id="c1b64-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c1b64-129">System.String</span></span>

## <span data-ttu-id="c1b64-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1b64-130">OUTPUTS</span></span>

### <span data-ttu-id="c1b64-131">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="c1b64-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="c1b64-132">Note</span><span class="sxs-lookup"><span data-stu-id="c1b64-132">NOTES</span></span>

## <span data-ttu-id="c1b64-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1b64-133">RELATED LINKS</span></span>
