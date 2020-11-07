---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 3bb2df6349c734e9802183c13eb39ae8ceafc50b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853030"
---
# <span data-ttu-id="bc849-101">New-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="bc849-101">New-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="bc849-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc849-102">SYNOPSIS</span></span>
<span data-ttu-id="bc849-103">Crea un oggetto Identity per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc849-103">Creates an identity object for an application gateway.</span></span> <span data-ttu-id="bc849-104">In questo modo si terrà riferimento all'identità assegnata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="bc849-104">This will hold reference to the user assigned identity.</span></span>

## <span data-ttu-id="bc849-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc849-105">SYNTAX</span></span>

```
New-AzApplicationGatewayIdentity -UserAssignedIdentityId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc849-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc849-106">DESCRIPTION</span></span>
<span data-ttu-id="bc849-107">Cmdlet **New-AzApplicationGatewayIdentity** crea un oggetto identità del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc849-107">**New-AzApplicationGatewayIdentity** cmdlet creates an application gateway identity object.</span></span>

## <span data-ttu-id="bc849-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc849-108">EXAMPLES</span></span>

### <span data-ttu-id="bc849-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bc849-109">Example 1</span></span>
```powershell
PS C:\> $identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\> $appgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $identity.Id
PS C:\> $gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $appgwIdentity <..>
```

<span data-ttu-id="bc849-110">In questo esempio creiamo un'identità assegnata dall'utente e quindi faccio riferimento a essa in un oggetto Identity usato con Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="bc849-110">In this example, we create a user assigned identity and then reference it in identity object used with Application Gateway.</span></span>

## <span data-ttu-id="bc849-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc849-111">PARAMETERS</span></span>

### <span data-ttu-id="bc849-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc849-112">-DefaultProfile</span></span>
<span data-ttu-id="bc849-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc849-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc849-114">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="bc849-114">-UserAssignedIdentityId</span></span>
<span data-ttu-id="bc849-115">ResourceId dell'identità assegnata dall'utente da assegnare al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc849-115">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="bc849-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bc849-116">-Confirm</span></span>
<span data-ttu-id="bc849-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc849-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc849-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc849-118">-WhatIf</span></span>
<span data-ttu-id="bc849-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc849-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc849-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc849-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc849-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc849-121">CommonParameters</span></span>
<span data-ttu-id="bc849-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc849-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc849-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc849-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc849-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc849-124">INPUTS</span></span>

### <span data-ttu-id="bc849-125">System. String</span><span class="sxs-lookup"><span data-stu-id="bc849-125">System.String</span></span>

## <span data-ttu-id="bc849-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc849-126">OUTPUTS</span></span>

### <span data-ttu-id="bc849-127">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="bc849-127">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="bc849-128">Note</span><span class="sxs-lookup"><span data-stu-id="bc849-128">NOTES</span></span>

## <span data-ttu-id="bc849-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc849-129">RELATED LINKS</span></span>
