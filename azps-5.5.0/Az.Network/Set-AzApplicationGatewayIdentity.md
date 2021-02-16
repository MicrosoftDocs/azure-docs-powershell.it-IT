---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: aa21ea0719c36e5b737b478657e0734eb21a3c3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186895"
---
# <span data-ttu-id="b1810-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="b1810-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="b1810-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1810-102">SYNOPSIS</span></span>
<span data-ttu-id="b1810-103">Aggiorna un'identità assegnata al gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="b1810-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="b1810-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1810-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1810-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b1810-105">DESCRIPTION</span></span>
<span data-ttu-id="b1810-106">Il cmdlet **Set-AzApplicationGatewayIdentity** aggiorna un'identità assegnata al gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="b1810-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="b1810-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1810-107">EXAMPLES</span></span>

### <span data-ttu-id="b1810-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b1810-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="b1810-109">In questo esempio viene assegnata un'identità assegnata a un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="b1810-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="b1810-110">Nota: questa identità deve avere accesso alla chiave da cui si fa riferimento ai certificati/segreti.</span><span class="sxs-lookup"><span data-stu-id="b1810-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="b1810-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1810-111">PARAMETERS</span></span>

### <span data-ttu-id="b1810-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1810-112">-ApplicationGateway</span></span>
<span data-ttu-id="b1810-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1810-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1810-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1810-114">-DefaultProfile</span></span>
<span data-ttu-id="b1810-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1810-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1810-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="b1810-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="b1810-117">ResourceId dell'identità assegnata all'utente da assegnare a Gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="b1810-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1810-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1810-118">-Confirm</span></span>
<span data-ttu-id="b1810-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1810-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1810-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1810-120">-WhatIf</span></span>
<span data-ttu-id="b1810-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1810-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1810-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1810-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1810-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1810-123">CommonParameters</span></span>
<span data-ttu-id="b1810-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1810-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1810-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1810-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1810-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="b1810-126">INPUTS</span></span>

### <span data-ttu-id="b1810-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1810-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="b1810-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b1810-128">System.String</span></span>

## <span data-ttu-id="b1810-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1810-129">OUTPUTS</span></span>

### <span data-ttu-id="b1810-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1810-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b1810-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="b1810-131">NOTES</span></span>

## <span data-ttu-id="b1810-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1810-132">RELATED LINKS</span></span>
