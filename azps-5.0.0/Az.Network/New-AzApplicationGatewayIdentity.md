---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: e32c0912026555f9b85a83720d1c7c48a5170f70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203138"
---
# <span data-ttu-id="61e7f-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="61e7f-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="61e7f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="61e7f-103">Crea un oggetto Identity per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61e7f-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="61e7f-104">In questo modo si terrà riferimento all'identità assegnata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="61e7f-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="61e7f-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61e7f-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61e7f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61e7f-106">DESCRIPTION</span></span>
<span data-ttu-id="61e7f-107">Cmdlet **New-AzApplicationGatewayIdentity** crea un oggetto identità del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61e7f-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="61e7f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61e7f-108">EXAMPLES</span></span>

### <span data-ttu-id="61e7f-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61e7f-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="61e7f-110">In questo esempio creiamo un'identità assegnata dall'utente e quindi faccio riferimento a essa in un oggetto Identity usato con Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="61e7f-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="61e7f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61e7f-111">PARAMETERS</span></span>

### <span data-ttu-id="61e7f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e7f-112">-DefaultProfile</span></span>
<span data-ttu-id="61e7f-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61e7f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61e7f-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="61e7f-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="61e7f-115">ResourceId dell'identità assegnata dall'utente da assegnare al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="61e7f-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="61e7f-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61e7f-116">-Confirm</span></span>
<span data-ttu-id="61e7f-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61e7f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61e7f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61e7f-118">-WhatIf</span></span>
<span data-ttu-id="61e7f-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61e7f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61e7f-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61e7f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61e7f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e7f-121">CommonParameters</span></span>
<span data-ttu-id="61e7f-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61e7f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e7f-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61e7f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e7f-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61e7f-124">INPUTS</span></span>

### <span data-ttu-id="61e7f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="61e7f-125">System.String</span></span>

## <span data-ttu-id="61e7f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61e7f-126">OUTPUTS</span></span>

### <span data-ttu-id="61e7f-127">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="61e7f-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="61e7f-128">Note</span><span class="sxs-lookup"><span data-stu-id="61e7f-128">NOTES</span></span>

## <span data-ttu-id="61e7f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61e7f-129">RELATED LINKS</span></span>
