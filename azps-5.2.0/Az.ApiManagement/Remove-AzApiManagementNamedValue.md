---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: c2cf7f46a7f7f73443a9d7d2b06dbfde943b28d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361350"
---
# <span data-ttu-id="b0042-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="b0042-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="b0042-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0042-102">SYNOPSIS</span></span>
<span data-ttu-id="b0042-103">Rimuove un valore denominato per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="b0042-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="b0042-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0042-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0042-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0042-105">DESCRIPTION</span></span>
<span data-ttu-id="b0042-106">Il cmdlet **Remove-AzApiManagementNamedValue** consente di rimuovere una gestione API di Azure **denominata value**.</span><span class="sxs-lookup"><span data-stu-id="b0042-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="b0042-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0042-107">EXAMPLES</span></span>

### <span data-ttu-id="b0042-108">Esempio 1: rimuovere il valore denominato</span><span class="sxs-lookup"><span data-stu-id="b0042-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="b0042-109">Questo comando rimuove il valore denominato che contiene l'ID Property11.</span><span class="sxs-lookup"><span data-stu-id="b0042-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="b0042-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0042-110">PARAMETERS</span></span>

### <span data-ttu-id="b0042-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b0042-111">-Context</span></span>
<span data-ttu-id="b0042-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b0042-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b0042-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b0042-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0042-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0042-114">-DefaultProfile</span></span>
<span data-ttu-id="b0042-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0042-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0042-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="b0042-116">-NamedValueId</span></span>
<span data-ttu-id="b0042-117">Identificatore del valore denominato esistente.</span><span class="sxs-lookup"><span data-stu-id="b0042-117">Identifier of existing named value.</span></span>
<span data-ttu-id="b0042-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b0042-118">This parameter is required.</span></span>

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

### <span data-ttu-id="b0042-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0042-119">-PassThru</span></span>
<span data-ttu-id="b0042-120">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="b0042-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b0042-121">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b0042-121">This parameter is optional.</span></span>
<span data-ttu-id="b0042-122">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="b0042-122">Default value is false.</span></span>

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

### <span data-ttu-id="b0042-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b0042-123">-Confirm</span></span>
<span data-ttu-id="b0042-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0042-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0042-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0042-125">-WhatIf</span></span>
<span data-ttu-id="b0042-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0042-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0042-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0042-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0042-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0042-128">CommonParameters</span></span>
<span data-ttu-id="b0042-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0042-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0042-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0042-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0042-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0042-131">INPUTS</span></span>

### <span data-ttu-id="b0042-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b0042-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b0042-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b0042-133">System.String</span></span>

### <span data-ttu-id="b0042-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b0042-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b0042-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0042-135">OUTPUTS</span></span>

### <span data-ttu-id="b0042-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0042-136">System.Boolean</span></span>

## <span data-ttu-id="b0042-137">Note</span><span class="sxs-lookup"><span data-stu-id="b0042-137">NOTES</span></span>

## <span data-ttu-id="b0042-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0042-138">RELATED LINKS</span></span>
