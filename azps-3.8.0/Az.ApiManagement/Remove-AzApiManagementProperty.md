---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
ms.openlocfilehash: 41ce5ae67bbc3b21b29740cde1503e474ebe9f8a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020097"
---
# <span data-ttu-id="d2ea9-101">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="d2ea9-101">Remove-AzApiManagementProperty</span></span>

## <span data-ttu-id="d2ea9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ea9-103">Rimuove una proprietà di gestione API.</span><span class="sxs-lookup"><span data-stu-id="d2ea9-103">Removes an API Management Property.</span></span>

## <span data-ttu-id="d2ea9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2ea9-104">SYNTAX</span></span>

```
Remove-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2ea9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2ea9-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ea9-106">Il cmdlet **Remove-AzApiManagementProperty** rimuove una **Proprietà** di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="d2ea9-106">The **Remove-AzApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="d2ea9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2ea9-107">EXAMPLES</span></span>

### <span data-ttu-id="d2ea9-108">Esempio 1: rimuovere una proprietà</span><span class="sxs-lookup"><span data-stu-id="d2ea9-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="d2ea9-109">Questo comando rimuove la proprietà con ID Property11.</span><span class="sxs-lookup"><span data-stu-id="d2ea9-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="d2ea9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2ea9-110">PARAMETERS</span></span>

### <span data-ttu-id="d2ea9-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d2ea9-111">-Context</span></span>
<span data-ttu-id="d2ea9-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d2ea9-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d2ea9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ea9-113">-DefaultProfile</span></span>
<span data-ttu-id="d2ea9-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2ea9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2ea9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2ea9-115">-PassThru</span></span>
<span data-ttu-id="d2ea9-116">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d2ea9-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="d2ea9-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="d2ea9-117">-PropertyId</span></span>
<span data-ttu-id="d2ea9-118">Specifica un ID della proprietà rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2ea9-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d2ea9-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d2ea9-119">-Confirm</span></span>
<span data-ttu-id="d2ea9-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2ea9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2ea9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2ea9-121">-WhatIf</span></span>
<span data-ttu-id="d2ea9-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2ea9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2ea9-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2ea9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2ea9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ea9-124">CommonParameters</span></span>
<span data-ttu-id="d2ea9-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ea9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ea9-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2ea9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ea9-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2ea9-127">INPUTS</span></span>

### <span data-ttu-id="d2ea9-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d2ea9-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d2ea9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d2ea9-129">System.String</span></span>

### <span data-ttu-id="d2ea9-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d2ea9-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d2ea9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2ea9-131">OUTPUTS</span></span>

### <span data-ttu-id="d2ea9-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2ea9-132">System.Boolean</span></span>

## <span data-ttu-id="d2ea9-133">Note</span><span class="sxs-lookup"><span data-stu-id="d2ea9-133">NOTES</span></span>

## <span data-ttu-id="d2ea9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2ea9-134">RELATED LINKS</span></span>

[<span data-ttu-id="d2ea9-135">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="d2ea9-135">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="d2ea9-136">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="d2ea9-136">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


