---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: a92387392c540c75cfa96ecaf4c4acf026ade9f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021909"
---
# <span data-ttu-id="d349b-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="d349b-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="d349b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d349b-102">SYNOPSIS</span></span>
<span data-ttu-id="d349b-103">Aggiunge un prodotto a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="d349b-103">Adds a product to a group.</span></span>

## <span data-ttu-id="d349b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d349b-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d349b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d349b-105">DESCRIPTION</span></span>
<span data-ttu-id="d349b-106">Il cmdlet **Add-AzApiManagementProductToGroup** aggiunge un prodotto a un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="d349b-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="d349b-107">In altre parole, questo cmdlet assegna un gruppo a un prodotto.</span><span class="sxs-lookup"><span data-stu-id="d349b-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="d349b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d349b-108">EXAMPLES</span></span>

### <span data-ttu-id="d349b-109">Esempio 1: aggiungere un prodotto a un gruppo</span><span class="sxs-lookup"><span data-stu-id="d349b-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="d349b-110">Questo comando aggiunge un prodotto a un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="d349b-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="d349b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d349b-111">PARAMETERS</span></span>

### <span data-ttu-id="d349b-112">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d349b-112">-Context</span></span>
<span data-ttu-id="d349b-113">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d349b-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="d349b-114">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d349b-114">This parameter is required.</span></span>

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

### <span data-ttu-id="d349b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d349b-115">-DefaultProfile</span></span>
<span data-ttu-id="d349b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d349b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d349b-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="d349b-117">-GroupId</span></span>
<span data-ttu-id="d349b-118">Specifica l'ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="d349b-118">Specifies the group ID.</span></span>
<span data-ttu-id="d349b-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d349b-119">This parameter is required.</span></span>

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

### <span data-ttu-id="d349b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d349b-120">-PassThru</span></span>
<span data-ttu-id="d349b-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="d349b-121">passthru</span></span>

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

### <span data-ttu-id="d349b-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="d349b-122">-ProductId</span></span>
<span data-ttu-id="d349b-123">Specifica l'ID prodotto.</span><span class="sxs-lookup"><span data-stu-id="d349b-123">Specifies the product ID.</span></span>
<span data-ttu-id="d349b-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d349b-124">This parameter is required.</span></span>

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

### <span data-ttu-id="d349b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d349b-125">CommonParameters</span></span>
<span data-ttu-id="d349b-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d349b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d349b-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d349b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d349b-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d349b-128">INPUTS</span></span>

### <span data-ttu-id="d349b-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d349b-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d349b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d349b-130">System.String</span></span>

### <span data-ttu-id="d349b-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d349b-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d349b-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d349b-132">OUTPUTS</span></span>

### <span data-ttu-id="d349b-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d349b-133">System.Boolean</span></span>

## <span data-ttu-id="d349b-134">Note</span><span class="sxs-lookup"><span data-stu-id="d349b-134">NOTES</span></span>

## <span data-ttu-id="d349b-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d349b-135">RELATED LINKS</span></span>

[<span data-ttu-id="d349b-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="d349b-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


