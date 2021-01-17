---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
ms.openlocfilehash: c115cd780750770e05bc55b1f70a7cfe33967fff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351127"
---
# <span data-ttu-id="3d580-101">New-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="3d580-101">New-AzMapsAccountKey</span></span>

## <span data-ttu-id="3d580-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d580-102">SYNOPSIS</span></span>
<span data-ttu-id="3d580-103">Rigenera una chiave dell'account.</span><span class="sxs-lookup"><span data-stu-id="3d580-103">Regenerates an account key.</span></span>

## <span data-ttu-id="3d580-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d580-104">SYNTAX</span></span>

### <span data-ttu-id="3d580-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3d580-105">NameParameterSet (Default)</span></span>
```
New-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d580-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d580-106">InputObjectParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d580-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d580-107">ResourceIdParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d580-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d580-108">DESCRIPTION</span></span>
<span data-ttu-id="3d580-109">Il cmdlet New-AzMapsAccountKey rigenera una chiave API per un account di Azure maps.</span><span class="sxs-lookup"><span data-stu-id="3d580-109">The New-AzMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="3d580-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d580-110">EXAMPLES</span></span>

### <span data-ttu-id="3d580-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3d580-111">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="3d580-112">Rigenera la chiave API primaria per il conto account nel gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3d580-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="3d580-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3d580-113">Example 2</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="3d580-114">Rigenera la chiave API secondaria per l'account di Azure Maps specificato.</span><span class="sxs-lookup"><span data-stu-id="3d580-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="3d580-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d580-115">PARAMETERS</span></span>

### <span data-ttu-id="3d580-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d580-116">-DefaultProfile</span></span>
<span data-ttu-id="3d580-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d580-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d580-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d580-118">-InputObject</span></span>
<span data-ttu-id="3d580-119">L'account di Maps viene inviato tramite pipe da Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="3d580-119">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d580-120">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="3d580-120">-KeyName</span></span>
<span data-ttu-id="3d580-121">Chiave dell'account Maps.</span><span class="sxs-lookup"><span data-stu-id="3d580-121">Maps Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d580-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d580-122">-Name</span></span>
<span data-ttu-id="3d580-123">Nome dell'account mappe.</span><span class="sxs-lookup"><span data-stu-id="3d580-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d580-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d580-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d580-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3d580-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d580-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d580-126">-ResourceId</span></span>
<span data-ttu-id="3d580-127">Mappe dell'account ResourceId.</span><span class="sxs-lookup"><span data-stu-id="3d580-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d580-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3d580-128">-Confirm</span></span>
<span data-ttu-id="3d580-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d580-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d580-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d580-130">-WhatIf</span></span>
<span data-ttu-id="3d580-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d580-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d580-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d580-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d580-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d580-133">CommonParameters</span></span>
<span data-ttu-id="3d580-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d580-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d580-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d580-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d580-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d580-136">INPUTS</span></span>

### <span data-ttu-id="3d580-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3d580-137">System.String</span></span>

### <span data-ttu-id="3d580-138">Microsoft. Azure. Commands. maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="3d580-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="3d580-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d580-139">OUTPUTS</span></span>

### <span data-ttu-id="3d580-140">Microsoft. Azure. Management. maps. Models. MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3d580-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="3d580-141">Note</span><span class="sxs-lookup"><span data-stu-id="3d580-141">NOTES</span></span>

## <span data-ttu-id="3d580-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d580-142">RELATED LINKS</span></span>
