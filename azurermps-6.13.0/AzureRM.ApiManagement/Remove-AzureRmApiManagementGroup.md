---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
ms.openlocfilehash: d297c4f8bb9999d60ec694c73aa723dd4afec58f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507739"
---
# <span data-ttu-id="6b9fd-101">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6b9fd-101">Remove-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="6b9fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b9fd-102">SYNOPSIS</span></span>
<span data-ttu-id="6b9fd-103">Rimuove un gruppo di gestione API esistente.</span><span class="sxs-lookup"><span data-stu-id="6b9fd-103">Removes an existing API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b9fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b9fd-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b9fd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b9fd-105">DESCRIPTION</span></span>
<span data-ttu-id="6b9fd-106">Il cmdlet **Remove-AzureRmApiManagementGroup** rimuove un gruppo di gestione API esistente.</span><span class="sxs-lookup"><span data-stu-id="6b9fd-106">The **Remove-AzureRmApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="6b9fd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b9fd-107">EXAMPLES</span></span>

### <span data-ttu-id="6b9fd-108">Esempio 1: rimuovere un gruppo di gestione esistente</span><span class="sxs-lookup"><span data-stu-id="6b9fd-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="6b9fd-109">Questo comando rimuove un gruppo di gestione esistente denominato Group0001 e non chiede conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="6b9fd-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="6b9fd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b9fd-110">PARAMETERS</span></span>

### <span data-ttu-id="6b9fd-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="6b9fd-111">-Context</span></span>
<span data-ttu-id="6b9fd-112">Specifica l'istanza di un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6b9fd-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6b9fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b9fd-113">-DefaultProfile</span></span>
<span data-ttu-id="6b9fd-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b9fd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b9fd-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="6b9fd-115">-GroupId</span></span>
<span data-ttu-id="6b9fd-116">Specifica l'identificatore di un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="6b9fd-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="6b9fd-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b9fd-117">-PassThru</span></span>
<span data-ttu-id="6b9fd-118">Indica che questo cmdlet restituisce un valore di $True se ha esito positivo oppure un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6b9fd-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="6b9fd-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b9fd-119">-Confirm</span></span>
<span data-ttu-id="6b9fd-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b9fd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b9fd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b9fd-121">-WhatIf</span></span>
<span data-ttu-id="6b9fd-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b9fd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b9fd-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b9fd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b9fd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b9fd-124">CommonParameters</span></span>
<span data-ttu-id="6b9fd-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b9fd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b9fd-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b9fd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b9fd-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b9fd-127">INPUTS</span></span>

### <span data-ttu-id="6b9fd-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6b9fd-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6b9fd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6b9fd-129">System.String</span></span>

### <span data-ttu-id="6b9fd-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6b9fd-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6b9fd-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b9fd-131">OUTPUTS</span></span>

### <span data-ttu-id="6b9fd-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b9fd-132">System.Boolean</span></span>

## <span data-ttu-id="6b9fd-133">Note</span><span class="sxs-lookup"><span data-stu-id="6b9fd-133">NOTES</span></span>

## <span data-ttu-id="6b9fd-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b9fd-134">RELATED LINKS</span></span>

[<span data-ttu-id="6b9fd-135">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6b9fd-135">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="6b9fd-136">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6b9fd-136">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="6b9fd-137">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6b9fd-137">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)

