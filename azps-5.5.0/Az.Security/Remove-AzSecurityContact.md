---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: b4cbecd2e29a0b70c7e62194df2364b22b33b462
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208266"
---
# <span data-ttu-id="4cbb5-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="4cbb5-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="4cbb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cbb5-102">SYNOPSIS</span></span>
<span data-ttu-id="4cbb5-103">Elimina un contatto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="4cbb5-103">Deletes a security contact.</span></span>

## <span data-ttu-id="4cbb5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cbb5-104">SYNTAX</span></span>

### <span data-ttu-id="4cbb5-105">SubscriptionLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="4cbb5-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cbb5-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cbb5-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cbb5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="4cbb5-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cbb5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4cbb5-108">DESCRIPTION</span></span>
<span data-ttu-id="4cbb5-109">Elimina un contatto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="4cbb5-109">Deletes a security contact.</span></span>

## <span data-ttu-id="4cbb5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cbb5-110">EXAMPLES</span></span>

### <span data-ttu-id="4cbb5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4cbb5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="4cbb5-112">Elimina il contatto di sicurezza "default1"</span><span class="sxs-lookup"><span data-stu-id="4cbb5-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="4cbb5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cbb5-113">PARAMETERS</span></span>

### <span data-ttu-id="4cbb5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cbb5-114">-DefaultProfile</span></span>
<span data-ttu-id="4cbb5-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4cbb5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cbb5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cbb5-116">-InputObject</span></span>
<span data-ttu-id="4cbb5-117">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="4cbb5-117">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cbb5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4cbb5-118">-Name</span></span>
<span data-ttu-id="4cbb5-119">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4cbb5-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cbb5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cbb5-120">-PassThru</span></span>
<span data-ttu-id="4cbb5-121">Restituisce se l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="4cbb5-121">Return whether the operation was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cbb5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cbb5-122">-ResourceId</span></span>
<span data-ttu-id="4cbb5-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="4cbb5-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cbb5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4cbb5-124">-Confirm</span></span>
<span data-ttu-id="4cbb5-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cbb5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cbb5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cbb5-126">-WhatIf</span></span>
<span data-ttu-id="4cbb5-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4cbb5-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cbb5-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4cbb5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cbb5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbb5-129">CommonParameters</span></span>
<span data-ttu-id="4cbb5-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cbb5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbb5-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4cbb5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbb5-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="4cbb5-132">INPUTS</span></span>

### <span data-ttu-id="4cbb5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4cbb5-133">System.String</span></span>

### <span data-ttu-id="4cbb5-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="4cbb5-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="4cbb5-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cbb5-135">OUTPUTS</span></span>

### <span data-ttu-id="4cbb5-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4cbb5-136">System.Boolean</span></span>

## <span data-ttu-id="4cbb5-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="4cbb5-137">NOTES</span></span>

## <span data-ttu-id="4cbb5-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cbb5-138">RELATED LINKS</span></span>
