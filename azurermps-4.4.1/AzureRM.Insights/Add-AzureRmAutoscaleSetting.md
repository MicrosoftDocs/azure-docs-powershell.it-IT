---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
ms.openlocfilehash: ee249d7379198a28cad22bf78a6c9ac1bf48f920
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688295"
---
# <span data-ttu-id="18874-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="18874-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="18874-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18874-102">SYNOPSIS</span></span>
<span data-ttu-id="18874-103">Crea un'impostazione di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="18874-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18874-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18874-104">SYNTAX</span></span>

### <span data-ttu-id="18874-105">Parametri per Add-AzureRmAutoscaleSetting cmdlet nella semantica di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="18874-105">Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics</span></span>
```
Add-AzureRmAutoscaleSetting -SettingSpec <PSAutoscaleSetting> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18874-106">Parametri per Add-AzureRmAutoscaleSetting cmdlet nella creazione di semantica</span><span class="sxs-lookup"><span data-stu-id="18874-106">Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18874-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18874-107">DESCRIPTION</span></span>
<span data-ttu-id="18874-108">Il cmdlet **Add-AzureRmAutoscaleSetting** crea un'impostazione di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="18874-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>

## <span data-ttu-id="18874-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18874-109">EXAMPLES</span></span>

### <span data-ttu-id="18874-110">Esempio 1: creare un'impostazione di scalabilità verticale</span><span class="sxs-lookup"><span data-stu-id="18874-110">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroup "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="18874-111">I primi due comandi usano New-AzureRmAutoscaleRule per creare due regole di scalabilità, $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="18874-111">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>

<span data-ttu-id="18874-112">Il terzo e il quarto comando usano New-AzureRmAutoscaleProfile per creare profili di scala, $Profile 1 e $Profile 2, usando $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="18874-112">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>

<span data-ttu-id="18874-113">Il comando finale crea un'impostazione di scalabilità verticale usando i profili in $Profile 1 e $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="18874-113">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="18874-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18874-114">PARAMETERS</span></span>

### <span data-ttu-id="18874-115">-AutoscaleProfiles</span><span class="sxs-lookup"><span data-stu-id="18874-115">-AutoscaleProfiles</span></span>
<span data-ttu-id="18874-116">Specifica un elenco di profili da aggiungere all'impostazione di scalabilità verticale oppure $Null per aggiungere nessun profilo.</span><span class="sxs-lookup"><span data-stu-id="18874-116">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18874-117">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="18874-117">-DisableSetting</span></span>
<span data-ttu-id="18874-118">Disabilita un'impostazione di scalabilità esistente.</span><span class="sxs-lookup"><span data-stu-id="18874-118">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="18874-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="18874-119">-Location</span></span>
<span data-ttu-id="18874-120">Specifica la posizione dell'impostazione di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="18874-120">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18874-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="18874-121">-Name</span></span>
<span data-ttu-id="18874-122">Specifica il nome dell'impostazione di scalabilità verticale da creare.</span><span class="sxs-lookup"><span data-stu-id="18874-122">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18874-123">-Notifiche</span><span class="sxs-lookup"><span data-stu-id="18874-123">-Notifications</span></span>
<span data-ttu-id="18874-124">Specifica un elenco di notifiche separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="18874-124">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18874-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="18874-125">-ResourceGroup</span></span>
<span data-ttu-id="18874-126">Specifica il nome del gruppo di risorse per la risorsa associata all'impostazione di scala.</span><span class="sxs-lookup"><span data-stu-id="18874-126">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

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

### <span data-ttu-id="18874-127">-SettingSpec</span><span class="sxs-lookup"><span data-stu-id="18874-127">-SettingSpec</span></span>
<span data-ttu-id="18874-128">Specifica un oggetto **AutoscaleSetting** .</span><span class="sxs-lookup"><span data-stu-id="18874-128">Specifies an **AutoscaleSetting** object.</span></span>
<span data-ttu-id="18874-129">Puoi usare il cmdlet Get-AzureRmAutoscaleSetting per ottenere un oggetto **AutoscaleSetting** oppure puoi crearne uno in uno script di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="18874-129">You can use the Get-AzureRmAutoscaleSetting cmdlet to get an **AutoscaleSetting** object or you can construct one in a Windows PowerShell script.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18874-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="18874-130">-TargetResourceId</span></span>
<span data-ttu-id="18874-131">Specifica l'ID della risorsa da scalare.</span><span class="sxs-lookup"><span data-stu-id="18874-131">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18874-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18874-132">-DefaultProfile</span></span>
<span data-ttu-id="18874-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18874-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18874-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18874-134">CommonParameters</span></span>
<span data-ttu-id="18874-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18874-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18874-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18874-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18874-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18874-137">INPUTS</span></span>

## <span data-ttu-id="18874-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18874-138">OUTPUTS</span></span>

### <span data-ttu-id="18874-139">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="18874-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="18874-140">Note</span><span class="sxs-lookup"><span data-stu-id="18874-140">NOTES</span></span>

## <span data-ttu-id="18874-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18874-141">RELATED LINKS</span></span>

[<span data-ttu-id="18874-142">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="18874-142">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="18874-143">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="18874-143">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="18874-144">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="18874-144">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="18874-145">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="18874-145">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


