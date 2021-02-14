---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
ms.openlocfilehash: 2b4133942a3aa7c4e9339579465942ade96c5709
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181798"
---
# <span data-ttu-id="cc1af-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="cc1af-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span></span>

## <span data-ttu-id="cc1af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc1af-102">SYNOPSIS</span></span>
<span data-ttu-id="cc1af-103">Ottiene un file desktop remoto per un'istanza del ruolo in un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="cc1af-103">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="cc1af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc1af-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceRemoteDesktopFile -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> -OutFile <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="cc1af-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cc1af-105">DESCRIPTION</span></span>
<span data-ttu-id="cc1af-106">Ottiene un file desktop remoto per un'istanza del ruolo in un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="cc1af-106">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="cc1af-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc1af-107">EXAMPLES</span></span>

### <span data-ttu-id="cc1af-108">Esempio 1: Ottenere un file RDP</span><span class="sxs-lookup"><span data-stu-id="cc1af-108">Example 1: Get an RDP file</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceRemoteDesktopFile -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0" -OutFile "C:\temp\ContosoFrontEnd_IN_0.rdp"
```

<span data-ttu-id="cc1af-109">Questo comando recupera un file RDP per l'istanza del ruolo denominata ContosoFrontEnd IN 0 del servizio cloud denominata ContosoCS che appartiene al gruppo di risorse \_ \_ denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="cc1af-109">This command gets an RDP file for the role instance named ContosoFrontEnd\_IN\_0 of cloud Service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="cc1af-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc1af-110">PARAMETERS</span></span>

### <span data-ttu-id="cc1af-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="cc1af-111">-CloudServiceName</span></span>
<span data-ttu-id="cc1af-112">.</span><span class="sxs-lookup"><span data-stu-id="cc1af-112">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc1af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc1af-113">-DefaultProfile</span></span>
<span data-ttu-id="cc1af-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cc1af-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc1af-115">-OutFile</span><span class="sxs-lookup"><span data-stu-id="cc1af-115">-OutFile</span></span>
<span data-ttu-id="cc1af-116">Percorso in cui scrivere il file di output</span><span class="sxs-lookup"><span data-stu-id="cc1af-116">Path to write output file to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc1af-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc1af-117">-PassThru</span></span>
<span data-ttu-id="cc1af-118">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="cc1af-118">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cc1af-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc1af-119">-ResourceGroupName</span></span>
<span data-ttu-id="cc1af-120">.</span><span class="sxs-lookup"><span data-stu-id="cc1af-120">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc1af-121">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="cc1af-121">-RoleInstanceName</span></span>
<span data-ttu-id="cc1af-122">Nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="cc1af-122">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc1af-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc1af-123">-SubscriptionId</span></span>
<span data-ttu-id="cc1af-124">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cc1af-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cc1af-125">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cc1af-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc1af-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc1af-126">CommonParameters</span></span>
<span data-ttu-id="cc1af-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc1af-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc1af-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cc1af-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc1af-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="cc1af-129">INPUTS</span></span>

## <span data-ttu-id="cc1af-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc1af-130">OUTPUTS</span></span>

### <span data-ttu-id="cc1af-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cc1af-131">System.Boolean</span></span>

## <span data-ttu-id="cc1af-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="cc1af-132">NOTES</span></span>

<span data-ttu-id="cc1af-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cc1af-133">ALIASES</span></span>

## <span data-ttu-id="cc1af-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc1af-134">RELATED LINKS</span></span>

