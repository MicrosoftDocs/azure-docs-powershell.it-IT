---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIdentity.md
ms.openlocfilehash: aa21ea0719c36e5b737b478657e0734eb21a3c3f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369823"
---
# <span data-ttu-id="cd22b-101">Set-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="cd22b-101">Set-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="cd22b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd22b-102">SYNOPSIS</span></span>
<span data-ttu-id="cd22b-103">Aggiorna un'identità assegnata al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cd22b-103">Updates a identity assigned to the application gateway.</span></span>

## <span data-ttu-id="cd22b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd22b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd22b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd22b-105">DESCRIPTION</span></span>
<span data-ttu-id="cd22b-106">Il cmdlet **set-AzApplicationGatewayIdentity** aggiorna un'identità assegnata al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cd22b-106">The **Set-AzApplicationGatewayIdentity** cmdlet updates an identity assigned to application gateway.</span></span>

## <span data-ttu-id="cd22b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd22b-107">EXAMPLES</span></span>

### <span data-ttu-id="cd22b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd22b-108">Example 1</span></span>
```powershell
PS C:\>$appgw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$appgwIdentity = Set-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id -ApplicationGateway $appgw
PS C:\>$updatedAppGw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="cd22b-109">In questo esempio viene assegnata un'identità assegnata all'utente a un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="cd22b-109">In this example, we assign a user assigned identity to an existing application gateway.</span></span>
<span data-ttu-id="cd22b-110">Nota: questa identità deve avere accesso al Vault di cui si fa riferimento ai certificati/segreti.</span><span class="sxs-lookup"><span data-stu-id="cd22b-110">Note: This identity should have access to the keyvault from which the certificates/secrets will be referenced.</span></span>

## <span data-ttu-id="cd22b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd22b-111">PARAMETERS</span></span>

### <span data-ttu-id="cd22b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd22b-112">-ApplicationGateway</span></span>
<span data-ttu-id="cd22b-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd22b-113">The applicationGateway</span></span>

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

### <span data-ttu-id="cd22b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd22b-114">-DefaultProfile</span></span>
<span data-ttu-id="cd22b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd22b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd22b-116">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="cd22b-116">-UserAssignedIdentityId</span></span>
<span data-ttu-id="cd22b-117">ResourceId dell'identità assegnata dall'utente da assegnare al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cd22b-117">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="cd22b-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd22b-118">-Confirm</span></span>
<span data-ttu-id="cd22b-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd22b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd22b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd22b-120">-WhatIf</span></span>
<span data-ttu-id="cd22b-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd22b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd22b-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd22b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd22b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd22b-123">CommonParameters</span></span>
<span data-ttu-id="cd22b-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd22b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd22b-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd22b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd22b-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd22b-126">INPUTS</span></span>

### <span data-ttu-id="cd22b-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd22b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="cd22b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cd22b-128">System.String</span></span>

## <span data-ttu-id="cd22b-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd22b-129">OUTPUTS</span></span>

### <span data-ttu-id="cd22b-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd22b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cd22b-131">Note</span><span class="sxs-lookup"><span data-stu-id="cd22b-131">NOTES</span></span>

## <span data-ttu-id="cd22b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd22b-132">RELATED LINKS</span></span>
