---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 92e241703723d055d18083daae5fe424933f7c3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521112"
---
# <span data-ttu-id="c68b6-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c68b6-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="c68b6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c68b6-102">SYNOPSIS</span></span>
<span data-ttu-id="c68b6-103">Rimuove una configurazione del provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="c68b6-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c68b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c68b6-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c68b6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c68b6-105">DESCRIPTION</span></span>
<span data-ttu-id="c68b6-106">Rimuove una configurazione del provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="c68b6-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="c68b6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c68b6-107">EXAMPLES</span></span>

### <span data-ttu-id="c68b6-108">Rimuove le impostazioni del provider di identità di Facebook dal servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c68b6-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="c68b6-109">Elimina la configurazione relativa alla configurazione del provider di identità di Facebook.</span><span class="sxs-lookup"><span data-stu-id="c68b6-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="c68b6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c68b6-110">PARAMETERS</span></span>

### <span data-ttu-id="c68b6-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c68b6-111">-Context</span></span>
<span data-ttu-id="c68b6-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c68b6-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c68b6-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c68b6-113">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c68b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c68b6-114">-DefaultProfile</span></span>
<span data-ttu-id="c68b6-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c68b6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c68b6-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c68b6-116">-PassThru</span></span>
<span data-ttu-id="c68b6-117">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c68b6-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c68b6-118">-Digitare</span><span class="sxs-lookup"><span data-stu-id="c68b6-118">-Type</span></span>
<span data-ttu-id="c68b6-119">Identificatore di un provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="c68b6-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="c68b6-120">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c68b6-120">This parameter is required.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c68b6-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c68b6-121">-Confirm</span></span>
<span data-ttu-id="c68b6-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c68b6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c68b6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c68b6-123">-WhatIf</span></span>
<span data-ttu-id="c68b6-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c68b6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c68b6-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c68b6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c68b6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c68b6-126">CommonParameters</span></span>
<span data-ttu-id="c68b6-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c68b6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c68b6-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c68b6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c68b6-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c68b6-129">INPUTS</span></span>

### <span data-ttu-id="c68b6-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c68b6-130">None</span></span>
<span data-ttu-id="c68b6-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c68b6-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c68b6-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c68b6-132">OUTPUTS</span></span>

### <span data-ttu-id="c68b6-133">bool</span><span class="sxs-lookup"><span data-stu-id="c68b6-133">bool</span></span>

## <span data-ttu-id="c68b6-134">Note</span><span class="sxs-lookup"><span data-stu-id="c68b6-134">NOTES</span></span>

## <span data-ttu-id="c68b6-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c68b6-135">RELATED LINKS</span></span>

[<span data-ttu-id="c68b6-136">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c68b6-136">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="c68b6-137">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c68b6-137">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="c68b6-138">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c68b6-138">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

