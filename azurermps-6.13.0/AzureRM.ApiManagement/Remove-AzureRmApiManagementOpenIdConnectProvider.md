---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6b4ccac87f963f9948c67d3162f1677b9860583b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507719"
---
# <span data-ttu-id="bb868-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bb868-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="bb868-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb868-102">SYNOPSIS</span></span>
<span data-ttu-id="bb868-103">Rimuove un provider OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="bb868-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb868-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb868-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb868-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb868-105">DESCRIPTION</span></span>
<span data-ttu-id="bb868-106">Il cmdlet **Remove-AzureRmApiManagementOpenIdConnectProvider** rimuove un provider OpenID Connect per la gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb868-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="bb868-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb868-107">EXAMPLES</span></span>

### <span data-ttu-id="bb868-108">Esempio 1: rimuovere un provider</span><span class="sxs-lookup"><span data-stu-id="bb868-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="bb868-109">Questo comando rimuove un provider con ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="bb868-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="bb868-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb868-110">PARAMETERS</span></span>

### <span data-ttu-id="bb868-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="bb868-111">-Context</span></span>
<span data-ttu-id="bb868-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="bb868-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb868-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb868-113">-DefaultProfile</span></span>
<span data-ttu-id="bb868-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb868-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb868-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="bb868-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="bb868-116">Specifica un ID del provider rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb868-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb868-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb868-117">-PassThru</span></span>
<span data-ttu-id="bb868-118">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bb868-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb868-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bb868-119">-Confirm</span></span>
<span data-ttu-id="bb868-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb868-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb868-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb868-121">-WhatIf</span></span>
<span data-ttu-id="bb868-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb868-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb868-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb868-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb868-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb868-124">CommonParameters</span></span>
<span data-ttu-id="bb868-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb868-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb868-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb868-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb868-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb868-127">INPUTS</span></span>

### <span data-ttu-id="bb868-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bb868-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bb868-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bb868-129">System.String</span></span>

### <span data-ttu-id="bb868-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bb868-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bb868-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb868-131">OUTPUTS</span></span>

### <span data-ttu-id="bb868-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb868-132">System.Boolean</span></span>

## <span data-ttu-id="bb868-133">Note</span><span class="sxs-lookup"><span data-stu-id="bb868-133">NOTES</span></span>

## <span data-ttu-id="bb868-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb868-134">RELATED LINKS</span></span>

[<span data-ttu-id="bb868-135">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bb868-135">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bb868-136">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bb868-136">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bb868-137">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bb868-137">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)

