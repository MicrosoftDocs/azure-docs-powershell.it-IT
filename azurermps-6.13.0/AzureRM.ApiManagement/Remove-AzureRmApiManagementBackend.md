---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: ef00a5140dc25065c05494211721c5773a9b5243
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507755"
---
# <span data-ttu-id="84ed9-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="84ed9-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="84ed9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84ed9-102">SYNOPSIS</span></span>
<span data-ttu-id="84ed9-103">Rimuove un backend.</span><span class="sxs-lookup"><span data-stu-id="84ed9-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84ed9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84ed9-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84ed9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84ed9-105">DESCRIPTION</span></span>
<span data-ttu-id="84ed9-106">Rimuove un backend specificato dall'identificatore dalla gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="84ed9-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="84ed9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84ed9-107">EXAMPLES</span></span>

### <span data-ttu-id="84ed9-108">Esempio 1: rimuovere il backend 123</span><span class="sxs-lookup"><span data-stu-id="84ed9-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="84ed9-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84ed9-109">PARAMETERS</span></span>

### <span data-ttu-id="84ed9-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="84ed9-110">-BackendId</span></span>
<span data-ttu-id="84ed9-111">Identificatore del backend esistente.</span><span class="sxs-lookup"><span data-stu-id="84ed9-111">Identifier of existing backend.</span></span>
<span data-ttu-id="84ed9-112">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="84ed9-112">This parameter is required.</span></span>

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

### <span data-ttu-id="84ed9-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="84ed9-113">-Context</span></span>
<span data-ttu-id="84ed9-114">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="84ed9-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="84ed9-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="84ed9-115">This parameter is required.</span></span>

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

### <span data-ttu-id="84ed9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84ed9-116">-DefaultProfile</span></span>
<span data-ttu-id="84ed9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84ed9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84ed9-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84ed9-118">-PassThru</span></span>
<span data-ttu-id="84ed9-119">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="84ed9-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="84ed9-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84ed9-120">This parameter is optional.</span></span>
<span data-ttu-id="84ed9-121">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="84ed9-121">Default value is false.</span></span>

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

### <span data-ttu-id="84ed9-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="84ed9-122">-Confirm</span></span>
<span data-ttu-id="84ed9-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84ed9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84ed9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84ed9-124">-WhatIf</span></span>
<span data-ttu-id="84ed9-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84ed9-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84ed9-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84ed9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84ed9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84ed9-127">CommonParameters</span></span>
<span data-ttu-id="84ed9-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84ed9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84ed9-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84ed9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84ed9-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84ed9-130">INPUTS</span></span>

### <span data-ttu-id="84ed9-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="84ed9-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="84ed9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="84ed9-132">System.String</span></span>

### <span data-ttu-id="84ed9-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="84ed9-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="84ed9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84ed9-134">OUTPUTS</span></span>

### <span data-ttu-id="84ed9-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="84ed9-135">System.Boolean</span></span>

## <span data-ttu-id="84ed9-136">Note</span><span class="sxs-lookup"><span data-stu-id="84ed9-136">NOTES</span></span>

## <span data-ttu-id="84ed9-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84ed9-137">RELATED LINKS</span></span>

[<span data-ttu-id="84ed9-138">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="84ed9-138">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="84ed9-139">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="84ed9-139">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="84ed9-140">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="84ed9-140">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="84ed9-141">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="84ed9-141">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="84ed9-142">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="84ed9-142">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
