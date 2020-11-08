---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021896"
---
# <span data-ttu-id="ead0e-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="ead0e-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="ead0e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ead0e-102">SYNOPSIS</span></span>
<span data-ttu-id="ead0e-103">Rimuove un VpnServerConfiguration esistente.</span><span class="sxs-lookup"><span data-stu-id="ead0e-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="ead0e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ead0e-104">SYNTAX</span></span>

### <span data-ttu-id="ead0e-105">ByVpnServerConfigurationName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ead0e-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead0e-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="ead0e-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead0e-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="ead0e-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ead0e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ead0e-108">DESCRIPTION</span></span>
<span data-ttu-id="ead0e-109">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="ead0e-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ead0e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ead0e-110">EXAMPLES</span></span>

### <span data-ttu-id="ead0e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ead0e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="ead0e-112">Il comando precedente consente di rimuovere un VpnServerConfiguration esistente.</span><span class="sxs-lookup"><span data-stu-id="ead0e-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="ead0e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ead0e-113">PARAMETERS</span></span>

### <span data-ttu-id="ead0e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead0e-114">-DefaultProfile</span></span>
<span data-ttu-id="ead0e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ead0e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ead0e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ead0e-116">-Force</span></span>
<span data-ttu-id="ead0e-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ead0e-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ead0e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ead0e-118">-InputObject</span></span>
<span data-ttu-id="ead0e-119">Oggetto vpnServerConfiguration da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ead0e-119">The vpnServerConfiguration object to be deleted.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ead0e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ead0e-120">-Name</span></span>
<span data-ttu-id="ead0e-121">Il nome vpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ead0e-121">The vpnServerConfiguration name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead0e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ead0e-122">-PassThru</span></span>
<span data-ttu-id="ead0e-123">Restituisce un oggetto che rappresenta l'elemento in cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ead0e-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="ead0e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ead0e-124">-ResourceGroupName</span></span>
<span data-ttu-id="ead0e-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ead0e-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead0e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ead0e-126">-ResourceId</span></span>
<span data-ttu-id="ead0e-127">ID risorsa di Azure per l'vpnServerConfiguration da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ead0e-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead0e-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ead0e-128">-Confirm</span></span>
<span data-ttu-id="ead0e-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ead0e-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead0e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead0e-130">-WhatIf</span></span>
<span data-ttu-id="ead0e-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ead0e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ead0e-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ead0e-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ead0e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead0e-133">CommonParameters</span></span>
<span data-ttu-id="ead0e-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ead0e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead0e-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ead0e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead0e-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ead0e-136">INPUTS</span></span>

### <span data-ttu-id="ead0e-137">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="ead0e-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="ead0e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ead0e-138">System.String</span></span>

## <span data-ttu-id="ead0e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ead0e-139">OUTPUTS</span></span>

### <span data-ttu-id="ead0e-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ead0e-140">System.Boolean</span></span>

## <span data-ttu-id="ead0e-141">Note</span><span class="sxs-lookup"><span data-stu-id="ead0e-141">NOTES</span></span>

## <span data-ttu-id="ead0e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ead0e-142">RELATED LINKS</span></span>
