---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 27e6be451d6141e322c47b2a84a28baf115839ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341488"
---
# <span data-ttu-id="77432-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="77432-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="77432-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77432-102">SYNOPSIS</span></span>
<span data-ttu-id="77432-103">Aggiunge un utente a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="77432-103">Adds a user to a group.</span></span>

## <span data-ttu-id="77432-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77432-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77432-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77432-105">DESCRIPTION</span></span>
<span data-ttu-id="77432-106">Il cmdlet **Add-AzApiManagementUserToGroup** aggiunge un utente a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="77432-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="77432-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77432-107">EXAMPLES</span></span>

### <span data-ttu-id="77432-108">Esempio 1: aggiungere un utente a un gruppo</span><span class="sxs-lookup"><span data-stu-id="77432-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="77432-109">Questo comando aggiunge un utente esistente a un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="77432-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="77432-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77432-110">PARAMETERS</span></span>

### <span data-ttu-id="77432-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="77432-111">-Context</span></span>
<span data-ttu-id="77432-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="77432-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="77432-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="77432-113">This parameter is required.</span></span>

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

### <span data-ttu-id="77432-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77432-114">-DefaultProfile</span></span>
<span data-ttu-id="77432-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77432-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77432-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="77432-116">-GroupId</span></span>
<span data-ttu-id="77432-117">Specifica l'ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="77432-117">Specifies the group ID.</span></span>
<span data-ttu-id="77432-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="77432-118">This parameter is required.</span></span>

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

### <span data-ttu-id="77432-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77432-119">-PassThru</span></span>
<span data-ttu-id="77432-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="77432-120">passthru</span></span>

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

### <span data-ttu-id="77432-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="77432-121">-UserId</span></span>
<span data-ttu-id="77432-122">Specifica l'ID utente.</span><span class="sxs-lookup"><span data-stu-id="77432-122">Specifies the user ID.</span></span>
<span data-ttu-id="77432-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="77432-123">This parameter is required.</span></span>

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

### <span data-ttu-id="77432-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77432-124">CommonParameters</span></span>
<span data-ttu-id="77432-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77432-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77432-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77432-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77432-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77432-127">INPUTS</span></span>

### <span data-ttu-id="77432-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="77432-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="77432-129">System. String</span><span class="sxs-lookup"><span data-stu-id="77432-129">System.String</span></span>

### <span data-ttu-id="77432-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="77432-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="77432-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77432-131">OUTPUTS</span></span>

### <span data-ttu-id="77432-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77432-132">System.Boolean</span></span>

## <span data-ttu-id="77432-133">Note</span><span class="sxs-lookup"><span data-stu-id="77432-133">NOTES</span></span>

## <span data-ttu-id="77432-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77432-134">RELATED LINKS</span></span>

[<span data-ttu-id="77432-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="77432-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="77432-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="77432-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


