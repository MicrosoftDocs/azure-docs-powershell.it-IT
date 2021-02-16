---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: e32c0912026555f9b85a83720d1c7c48a5170f70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202918"
---
# <span data-ttu-id="876fd-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="876fd-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="876fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="876fd-102">SYNOPSIS</span></span>
<span data-ttu-id="876fd-103">Crea un oggetto identità per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="876fd-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="876fd-104">In questo modo verrà con un riferimento all'identità assegnata all'utente.</span><span class="sxs-lookup"><span data-stu-id="876fd-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="876fd-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="876fd-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="876fd-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="876fd-106">DESCRIPTION</span></span>
<span data-ttu-id="876fd-107">Il cmdlet **New-AzApplicationGatewayIdentity crea** un oggetto identità del gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="876fd-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="876fd-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="876fd-108">EXAMPLES</span></span>

### <span data-ttu-id="876fd-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="876fd-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="876fd-110">In questo esempio viene creata un'identità assegnata a un utente a cui viene fatto riferimento nell'oggetto identità usato con Gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="876fd-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="876fd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="876fd-111">PARAMETERS</span></span>

### <span data-ttu-id="876fd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="876fd-112">-DefaultProfile</span></span>
<span data-ttu-id="876fd-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="876fd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="876fd-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="876fd-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="876fd-115">ResourceId dell'identità assegnata all'utente da assegnare a Gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="876fd-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="876fd-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="876fd-116">-Confirm</span></span>
<span data-ttu-id="876fd-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="876fd-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="876fd-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="876fd-118">-WhatIf</span></span>
<span data-ttu-id="876fd-119">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="876fd-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="876fd-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="876fd-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="876fd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="876fd-121">CommonParameters</span></span>
<span data-ttu-id="876fd-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="876fd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="876fd-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="876fd-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="876fd-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="876fd-124">INPUTS</span></span>

### <span data-ttu-id="876fd-125">System.String</span><span class="sxs-lookup"><span data-stu-id="876fd-125">System.String</span></span>

## <span data-ttu-id="876fd-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="876fd-126">OUTPUTS</span></span>

### <span data-ttu-id="876fd-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="876fd-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="876fd-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="876fd-128">NOTES</span></span>

## <span data-ttu-id="876fd-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="876fd-129">RELATED LINKS</span></span>
