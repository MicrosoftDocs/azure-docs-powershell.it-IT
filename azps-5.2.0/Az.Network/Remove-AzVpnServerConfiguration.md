---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345871"
---
# <span data-ttu-id="6e922-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e922-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="6e922-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6e922-102">SYNOPSIS</span></span>
<span data-ttu-id="6e922-103">Rimuove un VpnServerConfiguration esistente.</span><span class="sxs-lookup"><span data-stu-id="6e922-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="6e922-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e922-104">SYNTAX</span></span>

### <span data-ttu-id="6e922-105">ByVpnServerConfigurationName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6e922-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e922-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="6e922-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e922-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="6e922-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e922-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e922-108">DESCRIPTION</span></span>
<span data-ttu-id="6e922-109">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="6e922-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="6e922-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e922-110">EXAMPLES</span></span>

### <span data-ttu-id="6e922-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6e922-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="6e922-112">Il comando precedente consente di rimuovere un VpnServerConfiguration esistente.</span><span class="sxs-lookup"><span data-stu-id="6e922-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="6e922-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6e922-113">PARAMETERS</span></span>

### <span data-ttu-id="6e922-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e922-114">-DefaultProfile</span></span>
<span data-ttu-id="6e922-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e922-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e922-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6e922-116">-Force</span></span>
<span data-ttu-id="6e922-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="6e922-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6e922-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e922-118">-InputObject</span></span>
<span data-ttu-id="6e922-119">Oggetto vpnServerConfiguration da eliminare.</span><span class="sxs-lookup"><span data-stu-id="6e922-119">The vpnServerConfiguration object to be deleted.</span></span>

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

### <span data-ttu-id="6e922-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e922-120">-Name</span></span>
<span data-ttu-id="6e922-121">Il nome vpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6e922-121">The vpnServerConfiguration name.</span></span>

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

### <span data-ttu-id="6e922-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e922-122">-PassThru</span></span>
<span data-ttu-id="6e922-123">Restituisce un oggetto che rappresenta l'elemento in cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="6e922-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="6e922-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e922-124">-ResourceGroupName</span></span>
<span data-ttu-id="6e922-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6e922-125">The resource group name.</span></span>

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

### <span data-ttu-id="6e922-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e922-126">-ResourceId</span></span>
<span data-ttu-id="6e922-127">ID risorsa di Azure per l'vpnServerConfiguration da eliminare.</span><span class="sxs-lookup"><span data-stu-id="6e922-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

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

### <span data-ttu-id="6e922-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6e922-128">-Confirm</span></span>
<span data-ttu-id="6e922-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e922-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e922-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e922-130">-WhatIf</span></span>
<span data-ttu-id="6e922-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e922-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e922-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e922-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e922-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e922-133">CommonParameters</span></span>
<span data-ttu-id="6e922-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e922-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e922-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e922-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e922-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6e922-136">INPUTS</span></span>

### <span data-ttu-id="6e922-137">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e922-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="6e922-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6e922-138">System.String</span></span>

## <span data-ttu-id="6e922-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e922-139">OUTPUTS</span></span>

### <span data-ttu-id="6e922-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e922-140">System.Boolean</span></span>

## <span data-ttu-id="6e922-141">Note</span><span class="sxs-lookup"><span data-stu-id="6e922-141">NOTES</span></span>

## <span data-ttu-id="6e922-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e922-142">RELATED LINKS</span></span>
